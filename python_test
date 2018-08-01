import numpy as np
import pandas as pd

filepath1 = ""
filepath2 = ""
filepath3 =""
d = {'pctile': [1, 2, 3, 4], 'race': ['White', 'White', 'Black', 'White'], 
     'gender' : ["F", "M", "F", "F"], 's_family' : [0.370000, 0.5555, 0.666, 0.7777],
     's_indv' : [0.888, 0.999, 0.111, 0.222]}

df = pd.DataFrame(data=d)


print(df)
df = df.set_index([ 'pctile', 'race', 'gender']).unstack(0)
df = df.fillna(".")
print(df.reset_index(col_level=1).reset_index(col_level=1))
print(df.columns)

output

outcomes = ["indv", "family"]

skinnyoutcome = [""]

keepvars = ['s_' + var for var in outcomes]


data = pd.read_stata(filepath1 + "")
df = df[[keepvars, 'pctile', 'race', 'gender']]
df2 = df.unstack(level = ['s_family', 's_indv'])

#print(keepvars)