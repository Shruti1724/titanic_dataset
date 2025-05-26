# titanic_dataset
import pandas as pd
import numpy as np
df = pd.read_csv('/content/Titanic-Dataset.csv')
df.head()

df.isnull().sum()
df['Age'] = df['Age'].fillna(df['Age'].median())
df['Embarked'] = df['Embarked'].fillna(df['Embarked'].mode()[0])
df.isnull().sum()

df['Sex'] = df['Sex'].map({'male': 0, 'female': 1})
df = pd.get_dummies(df, columns=['Embarked'], drop_first=True)
df = df.drop(columns=['Name', 'Ticket'])

from sklearn.preprocessing import StandardScaler
cols_to_scale = ['Age', 'Fare', 'Parch', 'SibSp', 'Pclass']
scaler = StandardScaler()
df[cols_to_scale] = scaler.fit_transform(df[cols_to_scale])
df[cols_to_scale].describe()

import seaborn as sns
import matplotlib.pyplot as plt
sns.boxplot(data=df[['Age', 'Fare']])
plt.show()
