# 🐼 Marketing Package by Pandas Lovers 🐼
## HOLIDAY PACKAGE PREDICTION

![Green and Yellow Modern Playful Tour and Travel Banner-min](https://github.com/Astryon/final_project/assets/68798868/0e13866e-cc22-4637-bba1-a34fe43bccdc)


[![Open In Collab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1og6cvaGaytVXbDfEG2YFAhy9YhaIQPVY?usp=sharing#scrollTo=fQlFGqU0NjD-)
DATASET : [HOLIDAY PACKAGE PREDICTION](https://www.kaggle.com/datasets/susant4learning/holiday-package-purchase-prediction)

Kelompok Pandas lovers
1. Edgar Ariel Majied
2. Vionella Awanda Irsabadi
3. Teguh Ferdianto
4. R. Arnanda Adi Wijanarko
5. Sendy Boedhi
6. Jodhi Krisantus Sihalbu
7. Jannisah Dwi Rahhadiski
8. Faris Isham Wiryansyah

## 1. Handling Missing Value
```html
CustomerID                    0
ProdTaken                     0
Age                         226
TypeofContact                25
CityTier                      0
DurationOfPitch             251
Occupation                    0
Gender                        0
NumberOfPersonVisiting        0
NumberOfFollowups            45
ProductPitched                0
PreferredPropertyStar        26
MaritalStatus                 0
NumberOfTrips               140
Passport                      0
PitchSatisfactionScore        0
OwnCar                        0
NumberOfChildrenVisiting     66
Designation                   0
MonthlyIncome               233
dtype: int64
```
1.1. Kolom yang tidak sesuai ada 8, karena terdapat nilai kosong (missing value-nya ada 8) : 
1. Age (ganti mean), 
2. TypeofContact (di drop), 
3. DurationOfPitch (ganti median), 
4. NumberOfFollowups (ganti modus), 
5. PreferredPropertyStar (di drop), 
6. NumberOfTrips (di drop), 
7. NumberOfChildrenVisiting (di drop), 
8. MonthlyIncome (ganti median)

1.2. Setelah Drop dan imputasi missing value dengan mode, median & mean. Berikut untuk Tampilannya : 
```html
CustomerID                  0
ProdTaken                   0
Age                         0
TypeofContact               0
CityTier                    0
DurationOfPitch             0
Occupation                  0
Gender                      0
NumberOfPersonVisiting      0
NumberOfFollowups           0
ProductPitched              0
PreferredPropertyStar       0
MaritalStatus               0
NumberOfTrips               0
Passport                    0
PitchSatisfactionScore      0
OwnCar                      0
NumberOfChildrenVisiting    0
Designation                 0
MonthlyIncome               0
dtype: int64
```

## 2. Handling Invalid Data Types
2.1. Mengecek Data
```html
<class 'pandas.core.frame.DataFrame'>
Int64Index: 4631 entries, 0 to 4887
Data columns (total 20 columns):
 #   Column                    Non-Null Count  Dtype  
---  ------                    --------------  -----  
 0   CustomerID                4631 non-null   int64  
 1   ProdTaken                 4631 non-null   int64  
 2   Age                       4631 non-null   float64
 3   TypeofContact             4631 non-null   object 
 4   CityTier                  4631 non-null   int64  
 5   DurationOfPitch           4631 non-null   float64
 6   Occupation                4631 non-null   object 
 7   Gender                    4631 non-null   object 
 8   NumberOfPersonVisiting    4631 non-null   int64  
 9   NumberOfFollowups         4631 non-null   float64
 10  ProductPitched            4631 non-null   object 
 11  PreferredPropertyStar     4631 non-null   float64
 12  MaritalStatus             4631 non-null   object 
 13  NumberOfTrips             4631 non-null   float64
 14  Passport                  4631 non-null   int64  
 15  PitchSatisfactionScore    4631 non-null   int64  
 16  OwnCar                    4631 non-null   int64  
 17  NumberOfChildrenVisiting  4631 non-null   float64
 18  Designation               4631 non-null   object 
 19  MonthlyIncome             4631 non-null   float64
dtypes: float64(7), int64(7), object(6)
memory usage: 759.8+ KB
```

2.2. Mengubah tipe data dari float menjadi integer pada data yang di pilih

```html
df_new = df_new.astype({"Age":'int', "DurationOfPitch":'int','NumberOfFollowups':'int', 'PreferredPropertyStar':'int',
                        "NumberOfTrips":'int', "NumberOfChildrenVisiting":'int', "MonthlyIncome":'int'})
```

```html
<class 'pandas.core.frame.DataFrame'>
Int64Index: 4631 entries, 0 to 4887
Data columns (total 20 columns):
 #   Column                    Non-Null Count  Dtype 
---  ------                    --------------  ----- 
 0   CustomerID                4631 non-null   int64 
 1   ProdTaken                 4631 non-null   int64 
 2   Age                       4631 non-null   int64 
 3   TypeofContact             4631 non-null   object
 4   CityTier                  4631 non-null   int64 
 5   DurationOfPitch           4631 non-null   int64 
 6   Occupation                4631 non-null   object
 7   Gender                    4631 non-null   object
 8   NumberOfPersonVisiting    4631 non-null   int64 
 9   NumberOfFollowups         4631 non-null   int64 
 10  ProductPitched            4631 non-null   object
 11  PreferredPropertyStar     4631 non-null   int64 
 12  MaritalStatus             4631 non-null   object
 13  NumberOfTrips             4631 non-null   int64 
 14  Passport                  4631 non-null   int64 
 15  PitchSatisfactionScore    4631 non-null   int64 
 16  OwnCar                    4631 non-null   int64 
 17  NumberOfChildrenVisiting  4631 non-null   int64 
 18  Designation               4631 non-null   object
 19  MonthlyIncome             4631 non-null   int64 
dtypes: int64(14), object(6)
memory usage: 759.8+ KB
```

## 3. Handling Duplicated Data
```html
Banyak data dan kolom :  (4631, 20)
Jumlah ID Customer duplikat :  0
Jumlah data duplikat :  0
```
Tidak ada Duplikat Data

## 4. Handling Invalid Value

4.1. Mengubah value Fe Male menjadi Female

4.2. Jumlahnya menjadi : 

```html
Male      2765
Female    1866
Name: Gender, dtype: int64
```


## 5. Handling Outliers
![Screenshot 2023-06-03 163423](https://github.com/Astryon/Stage2_Final_Project/assets/68798868/524db16d-61a9-45f9-903d-2d152dd7cc40)

5.1. Terdapat Outliers pada Age, DurationOfPitch, dan MonthlyIncome. 

5.2. Lalu dilakukan Filltering menggunakan Z-Score Sehingga diperoleh data sebagai berikut : 

![Screenshot 2023-06-03 163800](https://github.com/Astryon/Stage2_Final_Project/assets/68798868/d8b37d78-4655-4f1c-9469-0b5686ec3b86)

   Didapati nilai Filltering menggunakan Z-Scorenya yaitu 4617. 

5.3. Berikut ini merupakan Distribusi data setelan filtering Outliers : 
![Screenshot 2023-06-03 163931](https://github.com/Astryon/Stage2_Final_Project/assets/68798868/0d1b3f19-9ffc-4c09-a521-a50eefea775e)

## 6. Feature Transformation

6.1. DurationOfPitch dan MonthlyIncome dinormalisasi/re-scale dan Age distandarisasi (karena distribusi datanya sudah mendekati normal)

6.2. Berikut ini adalah data setelah normalisasi/re-scale dan standarisasi
![Screenshot 2023-06-03 164308](https://github.com/Astryon/Stage2_Final_Project/assets/68798868/31becff0-961d-4020-bf69-8cdada1279e2)

6.3. Describe Data setelah Transformation : 

![image](https://github.com/Astryon/Stage2_Final_Project/assets/68798868/a5a00997-ce05-444f-9bc3-a954d8b4260f)


## 7. Feature Encoding
7.1. Onehots encoder pada Occupation dan TypeofContact

![image](https://github.com/Astryon/Stage2_Final_Project/assets/68798868/2a5aa41c-a6c4-4d2e-a226-a66c8db3f27d)


7.2. Label encoder pada Gender

![image](https://github.com/Astryon/Stage2_Final_Project/assets/68798868/a8701da7-6850-4646-bdb2-452a1546bc0e)

7.3. Product Pick 

![Screenshot 2023-06-03 164512](https://github.com/Astryon/Stage2_Final_Project/assets/68798868/82e2b907-2598-4cbe-9fb0-ed187bc2dbc6)

7.4. Membuat function Product dan menjalankannya 

![Screenshot 2023-06-03 164734](https://github.com/Astryon/Stage2_Final_Project/assets/68798868/2b043d93-fea3-443f-8a9b-4278c334afb2)

7.5. Membuat Function dan Kolom Baru pada status : 

![Screenshot 2023-06-03 164928](https://github.com/Astryon/Stage2_Final_Project/assets/68798868/5a30e948-fa66-4c87-bc1d-6e9339c7b081)

7.6. Membuat Function Designation

![image](https://github.com/Astryon/Stage2_Final_Project/assets/68798868/d3a1b887-075f-4c90-b0b1-d2a3de885d1b)

7.7. Hasil Datanya : 

![image](https://github.com/Astryon/Stage2_Final_Project/assets/68798868/6e23b50a-4701-42e7-9116-587594fd227b)

## 8. Feature Selection
8.1. Visualisasi Korelasi Data : 

![image](https://github.com/Astryon/Stage2_Final_Project/assets/68798868/ffa529f4-76b3-4434-874f-1ca29c2da9f1)

![image](https://github.com/Astryon/Stage2_Final_Project/assets/68798868/a3d37dbe-9813-4503-8752-b22f7dcc7012)

8.2. Melakukan drop feature yang tidak terpakai atau korelasinya di bawah < 0,1 / -0,1 : 

![image](https://github.com/Astryon/Stage2_Final_Project/assets/68798868/ac0a52da-4755-4cd0-995b-16215e156b1d)

8.3. Melakukan ubah posisi ProdTaken ke paling kanan dan running kembali korelasinya : 

![image](https://github.com/Astryon/Stage2_Final_Project/assets/68798868/20965001-40b4-4645-963a-727f4ebbabc8)

8.4. Melakukan cek kembali 

![image](https://github.com/Astryon/Stage2_Final_Project/assets/68798868/a7d73591-d3de-44ed-84b5-96795b16b82f)

## 9. Splitting Data & Handling Class Imbalance
9.1. Membagi data train dan test (70:30)

![image](https://github.com/Astryon/Stage2_Final_Project/assets/68798868/af9800fc-41f0-4f44-b63d-6529698cd70d)

Didapati nilai baris train set yaitu : 3231 dan nilai untuk baris test set yaitu : 1386 

9.2. Cek fitur train set

![image](https://github.com/Astryon/Stage2_Final_Project/assets/68798868/d4e8a054-f967-4bf6-9845-980d04a2cc49)

9.3. Split x dan y

9.4. Oversampling menggunakan SMOTE, di dapati nilai sebagai berikut : 

![image](https://github.com/Astryon/Stage2_Final_Project/assets/68798868/619e2342-393e-4fa0-a621-b1d4262870f2)

9.5. Berikut untuk jumlah baris train dan test untuk x dan y nya : 

![image](https://github.com/Astryon/Stage2_Final_Project/assets/68798868/037ffecd-b8ef-482a-b0f2-d116458023b5)

# Terima Kasih :) 🐼














