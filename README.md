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

## Handling Missing Value
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
Kolom yang tidak sesuai ada 8, karena terdapat nilai kosong (missing value-nya ada 8) : 
1. Age (ganti mean), 
2. TypeofContact (di drop), 
3. DurationOfPitch (ganti median), 
4. NumberOfFollowups (ganti modus), 
5. PreferredPropertyStar (di drop), 
6. NumberOfTrips (di drop), 
7. NumberOfChildrenVisiting (di drop), 
8. MonthlyIncome (ganti median)

Setelah Drop dan imputasi missing value dengan mode, median & mean. Berikut untuk Tampilannya : 
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

## Handling Duplicated Data
```html
Banyak data dan kolom :  (4631, 20)
Jumlah ID Customer duplikat :  0
Jumlah data duplikat :  0
```
Tidak ada Duplikat Data

## Handling Invalid Value
1. Mengubah gender yang pengisian Fe Male menjadi Female
```html
Male      2765
Female    1866
Name: Gender, dtype: int64
```
Sehingga diperoleh data untuk Male (Pria) sebanyak 2765 Orang dan untuk Female (Wanita) sebanyak 1866 Orang

2. Mengubah value Unmarried & Divorced menjadi Single
```html
Single     2427
Married    2204
Name: MaritalStatus, dtype: int64
```
Sehingga diperoleh data untuk Single sebanyak 2427 Orang dan untuk Married sebanyak 2204 Orang

## Handling Outliers
![Screenshot 2023-06-03 163423](https://github.com/Astryon/Stage2_Final_Project/assets/68798868/524db16d-61a9-45f9-903d-2d152dd7cc40)

1. Terdapat Outliers pada Age, DurationOfPitch, dan MonthlyIncome. 

2. Lalu dilakukan Filltering menggunakan Z-Score Sehingga diperoleh data sebagai berikut : 

![Screenshot 2023-06-03 163800](https://github.com/Astryon/Stage2_Final_Project/assets/68798868/d8b37d78-4655-4f1c-9469-0b5686ec3b86)

   Didapati nilai Filltering menggunakan Z-Scorenya yaitu 4617. 

3. Berikut ini merupakan Distribusi data setelan filtering Outliers : 
![Screenshot 2023-06-03 163931](https://github.com/Astryon/Stage2_Final_Project/assets/68798868/0d1b3f19-9ffc-4c09-a521-a50eefea775e)

## Feature Transformation

1. DurationOfPitch dan MonthlyIncome dinormalisasi/re-scale dan Age distandarisasi (karena distribusi datanya sudah mendekati normal)
2. Berikut ini adalah data setelah normalisasi/re-scale dan standarisasi
![Screenshot 2023-06-03 164308](https://github.com/Astryon/Stage2_Final_Project/assets/68798868/31becff0-961d-4020-bf69-8cdada1279e2)

3. Describe Data setelah Transformation : 

![image](https://github.com/Astryon/Stage2_Final_Project/assets/68798868/a5a00997-ce05-444f-9bc3-a954d8b4260f)


## Feature Encoding
1. Onehots encoder pada Occupation dan TypeofContact

![image](https://github.com/Astryon/Stage2_Final_Project/assets/68798868/2a5aa41c-a6c4-4d2e-a226-a66c8db3f27d)


3. Label encoder pada Gender

![image](https://github.com/Astryon/Stage2_Final_Project/assets/68798868/a8701da7-6850-4646-bdb2-452a1546bc0e)

4. Product Pick 

![Screenshot 2023-06-03 164512](https://github.com/Astryon/Stage2_Final_Project/assets/68798868/82e2b907-2598-4cbe-9fb0-ed187bc2dbc6)

5. Membuat function Product dan menjalankannya 

![Screenshot 2023-06-03 164734](https://github.com/Astryon/Stage2_Final_Project/assets/68798868/2b043d93-fea3-443f-8a9b-4278c334afb2)

6. Membuat Function dan Kolom Baru pada status : 

![Screenshot 2023-06-03 164928](https://github.com/Astryon/Stage2_Final_Project/assets/68798868/5a30e948-fa66-4c87-bc1d-6e9339c7b081)

7. Membuat Function Designation

![image](https://github.com/Astryon/Stage2_Final_Project/assets/68798868/d3a1b887-075f-4c90-b0b1-d2a3de885d1b)

8. Hasil Datanya : 

![image](https://github.com/Astryon/Stage2_Final_Project/assets/68798868/6e23b50a-4701-42e7-9116-587594fd227b)

## Feature Selection






