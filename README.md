# Ex-01_DS_Data_Cleansing


## AIM
To read the given data and perform data cleaning and save the cleaned data to a file. 

# Explanation
Data cleaning is the process of preparing data for analysis by removing or modifying data that is incorrect ,incompleted , irrelevant , duplicated or improperly formatted. 
Data cleaning is not simply about erasing data ,but rather finding a way to maximize datasets accuracy without necessarily deleting the information. 

# ALGORITHM
### STEP 1
Read the given Data
### STEP 2
Get the information about the data
### STEP 3
Remove the null values from the data
### STEP 4
Save the Clean data to the file

# CODE 
```
import pandas as pd
df=pd.read_csv('/content/SAMPLEDS.csv')
df
df.shape
df.describe()
df.isnull().sum()
df.dropna(how='any').shape
x=df.dropna(how='any')
x
df.dropna(how='all').shape
tot = df.dropna(subset=['TOTAL'],how='any')
tot
m = df.dropna(subset=['M4'],how='any')
m
tot = df.dropna(subset=['M1','M2','M3','M4'],how='any')
tot
df.fillna(0)
df
df.fillna(method='ffill')
df.fillna(method='bfill')
mn=df.TOTAL.mean()
mn
df.TOTAL.fillna(mn,inplace=True)
df
l=df.M1.interpolate()
l
df.M1.fillna(l,inplace=True)
df
mn=df.TOTAL.median()
mn
df.TOTAL.fillna(mn,inplace=True)
df
l=df.M1.interpolate()
l
df.M1.fillna(l,inplace=True)
df
mn=df.TOTAL.mode()
mn
df.drop_duplicates(inplace=True)
df
df['cd']=pd.to_datetime(df['DOB'])
df
for x in df.index: if df.loc[x,"AVG"]>100: df.drop(x,inplace=True)
df
```
## OUTPUT:
![Screenshot 2023-09-09 152748](https://github.com/Balachandran143/ODD2023-Datascience-Ex01/assets/118886489/a95c0e42-bb87-4669-9689-62605280a990)
![Screenshot 2023-09-09 153104](https://github.com/Balachandran143/ODD2023-Datascience-Ex01/assets/118886489/332952e2-9c3b-41bb-a838-2c19c984223c)
![Screenshot 2023-09-09 153138](https://github.com/Balachandran143/ODD2023-Datascience-Ex01/assets/118886489/415fd883-74ad-46f8-a486-97a1624b3925)
![Screenshot 2023-09-09 153208](https://github.com/Balachandran143/ODD2023-Datascience-Ex01/assets/118886489/b5440dae-687f-4b4e-a742-a83e13d26e55)
![Screenshot 2023-09-09 153212](https://github.com/Balachandran143/ODD2023-Datascience-Ex01/assets/118886489/243955b2-8d68-4727-8c57-b599c1fb154a)
![Screenshot 2023-09-09 153233](https://github.com/Balachandran143/ODD2023-Datascience-Ex01/assets/118886489/9be2df76-8da7-4dfd-9657-d1119ef94ec9)
![Screenshot 2023-09-09 153239](https://github.com/Balachandran143/ODD2023-Datascience-Ex01/assets/118886489/f97c43d5-894b-4297-83d6-daa0a381445d)
![Screenshot 2023-09-09 153257](https://github.com/Balachandran143/ODD2023-Datascience-Ex01/assets/118886489/c1e5c51a-8f86-42aa-9481-be62ed118b47)
![Screenshot 2023-09-09 153309](https://github.com/Balachandran143/ODD2023-Datascience-Ex01/assets/118886489/45aa4e84-5eca-47fc-840f-704ee5d95e21)
![Screenshot 2023-09-09 153321](https://github.com/Balachandran143/ODD2023-Datascience-Ex01/assets/118886489/466e7b9c-c7bc-4a1c-805c-9a7ff9be1587)
![Screenshot 2023-09-09 153336](https://github.com/Balachandran143/ODD2023-Datascience-Ex01/assets/118886489/b682c3d5-9497-4753-ac7b-b1db64d294f7)
![Screenshot 2023-09-09 153355](https://github.com/Balachandran143/ODD2023-Datascience-Ex01/assets/118886489/976f5a6f-f893-4519-a160-c4f792522a5c)
![Screenshot 2023-09-09 153425](https://github.com/Balachandran143/ODD2023-Datascience-Ex01/assets/118886489/a5d9ddb1-17f5-410f-938d-1a70141aac6b)
![Screenshot 2023-09-09 153434](https://github.com/Balachandran143/ODD2023-Datascience-Ex01/assets/118886489/09aba96a-e2b4-45e2-a8db-8443c57a303a)
![Screenshot 2023-09-09 153442](https://github.com/Balachandran143/ODD2023-Datascience-Ex01/assets/118886489/b9e661ba-bc1d-4580-a130-868d18ea56eb)
![Screenshot 2023-09-09 153457](https://github.com/Balachandran143/ODD2023-Datascience-Ex01/assets/118886489/8ce63778-5681-428a-914e-90e33f042cf1)
![Screenshot 2023-09-09 153513](https://github.com/Balachandran143/ODD2023-Datascience-Ex01/assets/118886489/bf61f7b9-f796-4376-b6c7-4c2a076993fd)
![Screenshot 2023-09-09 153519](https://github.com/Balachandran143/ODD2023-Datascience-Ex01/assets/118886489/072b06fe-e61e-4b89-b5cd-3fb2d70d9c13)
![Screenshot 2023-09-09 153532](https://github.com/Balachandran143/ODD2023-Datascience-Ex01/assets/118886489/6f09fa19-987d-46c4-96cc-ffca03d7fe31)
![Screenshot 2023-09-09 153547](https://github.com/Balachandran143/ODD2023-Datascience-Ex01/assets/118886489/73b3c5e8-6fa1-4238-915c-2a5852ad72fd)
![Screenshot 2023-09-09 153550](https://github.com/Balachandran143/ODD2023-Datascience-Ex01/assets/118886489/35a30bd1-858f-42b3-a56c-faab0db586a3)
![Screenshot 2023-09-09 153616](https://github.com/Balachandran143/ODD2023-Datascience-Ex01/assets/118886489/62e44320-5387-404c-adcb-08b2033e530f)
![Screenshot 2023-09-09 153718](https://github.com/Balachandran143/ODD2023-Datascience-Ex01/assets/118886489/e6705cf6-6207-4231-902d-7b262c63dc91)
![Screenshot 2023-09-09 153749](https://github.com/Balachandran143/ODD2023-Datascience-Ex01/assets/118886489/7f42c701-965c-4965-b5f8-ecbe1216ca48)

## RESULT:
Thus,the given data is cleansed and the cleaned data is saved into the file.


