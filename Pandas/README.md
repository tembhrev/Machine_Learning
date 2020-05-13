Numpy vs Panda (Package)

Array can be matrix or vector
matrix can be 2D
vector can be 1D

matrix(numpy) can hold one type of data in two dimensional structure
dataframe(pandas)- It can hold multiple series which are of different data types, uses basic concepts of numpy.For a series we can assign custom index position values however for a vector that is not possible.We can customize the index values using letters instead of numbers for  the first column
Data frame consisted of multiple series within it.we can merge the common column
matrix in a numpy array is created by using multiple vectors within it

Functionalities of Pandas Data Frame
-------------------------------------
import pandas as pd

three ways you can convert list, dict and array in series

Pandas dataframes and indexing

np.random.seed(100) - will ensure you will see same random values

dataframe.drop('Score6', axis=1)
1 = column
o = row

dataframe.drop('Score6',axis=1,inplace=True)

selection of rows:
------------------
dataframe.loc['F']
dataframe.iloc[2] - indexed location
dataframe.loc['A','Score1'] - Selecting row and column
dataframe.loc[['A','B'],['Score1','Score2']] - Subsetting ,selecting 2 rows and 2 columns
dataframe > 0.5 - Set of boolean values

Indexing in Depth
-----------------
dataframe.reset_index() - reset the original indexes

dataframe.set_index("Countries",inplace = True)-Setting new column but have to use "inplace" to get the changes reflected

Dealing Missing Data and group-by options
------------------------------------------
dataframe.dropna()
dataframe.dropna(axis=1)  #by column
dataframe.dropna(thresh=2) #if 2 values are not Nan in the row
dataframe.fillna(value=0)

pd.merge(dafa1, dafa2, how = "inner", on = "CustID")
how = outer, left, right

Merge happens based on common column
Join happens based on index

dafa1.join(dafa2)

Basic Operations
----------------
dataframe.head(3)  #Displays first 3 rows
dataframe['column Name'].unique()
dataframe['column Name'].nunique()
dataframe['column Name'].value_counts()
dataframe['column Name'].apply()
dataframe['column Name'].apply(len)
dataframe['column Name'].sum()

del dataframe['column Name']

dataframe.columns
dataframe.index

dataframe.sort_values(by='column Name')
dataframe.isnull()
dataframe.dropna()
dataframe.fillna('Not nan')
dataframe = pd.read_csv('file_name.csv')
dataframe = pd.to_csv('file_name.csv', index=False) #will not store the default index values
dataframe = pd.read_excel('file_name'.xlsx, sheet_name = 'Data1')
dataframe = pd.to_excel('file_name'.xlsx, sheet_name = 'sheet1')