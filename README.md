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

## 2. Handling Duplicated Data
```html
Banyak data dan kolom :  (4631, 20)
Jumlah ID Customer duplikat :  0
Jumlah data duplikat :  0
```
Tidak ada Duplikat Data

## 3. Handling Invalid Value
3.1. Mengubah gender yang pengisian Fe Male menjadi Female
```html
Male      2765
Female    1866
Name: Gender, dtype: int64
```
Sehingga diperoleh data untuk Male (Pria) sebanyak 2765 Orang dan untuk Female (Wanita) sebanyak 1866 Orang

3.2. Mengubah value Unmarried & Divorced menjadi Single
```html
Single     2427
Married    2204
Name: MaritalStatus, dtype: int64
```
Sehingga diperoleh data untuk Single sebanyak 2427 Orang dan untuk Married sebanyak 2204 Orang

## 4. Handling Outliers
![Screenshot 2023-06-03 163423](https://github.com/Astryon/Stage2_Final_Project/assets/68798868/524db16d-61a9-45f9-903d-2d152dd7cc40)

4.1. Terdapat Outliers pada Age, DurationOfPitch, dan MonthlyIncome. 

4.2. Lalu dilakukan Filltering menggunakan Z-Score Sehingga diperoleh data sebagai berikut : 

![Screenshot 2023-06-03 163800](https://github.com/Astryon/Stage2_Final_Project/assets/68798868/d8b37d78-4655-4f1c-9469-0b5686ec3b86)

   Didapati nilai Filltering menggunakan Z-Scorenya yaitu 4617. 

4.3. Berikut ini merupakan Distribusi data setelan filtering Outliers : 
![Screenshot 2023-06-03 163931](https://github.com/Astryon/Stage2_Final_Project/assets/68798868/0d1b3f19-9ffc-4c09-a521-a50eefea775e)

## 5. Feature Transformation

5.1. DurationOfPitch dan MonthlyIncome dinormalisasi/re-scale dan Age distandarisasi (karena distribusi datanya sudah mendekati normal)

5.2. Berikut ini adalah data setelah normalisasi/re-scale dan standarisasi
![Screenshot 2023-06-03 164308](https://github.com/Astryon/Stage2_Final_Project/assets/68798868/31becff0-961d-4020-bf69-8cdada1279e2)

5.3. Describe Data setelah Transformation : 

![image](https://github.com/Astryon/Stage2_Final_Project/assets/68798868/a5a00997-ce05-444f-9bc3-a954d8b4260f)


## 6. Feature Encoding
6.1. Onehots encoder pada Occupation dan TypeofContact

![image](https://github.com/Astryon/Stage2_Final_Project/assets/68798868/2a5aa41c-a6c4-4d2e-a226-a66c8db3f27d)


6.2. Label encoder pada Gender

![image](https://github.com/Astryon/Stage2_Final_Project/assets/68798868/a8701da7-6850-4646-bdb2-452a1546bc0e)

6.3. Product Pick 

![Screenshot 2023-06-03 164512](https://github.com/Astryon/Stage2_Final_Project/assets/68798868/82e2b907-2598-4cbe-9fb0-ed187bc2dbc6)

6.4. Membuat function Product dan menjalankannya 

![Screenshot 2023-06-03 164734](https://github.com/Astryon/Stage2_Final_Project/assets/68798868/2b043d93-fea3-443f-8a9b-4278c334afb2)

6.5. Membuat Function dan Kolom Baru pada status : 

![Screenshot 2023-06-03 164928](https://github.com/Astryon/Stage2_Final_Project/assets/68798868/5a30e948-fa66-4c87-bc1d-6e9339c7b081)

6.6. Membuat Function Designation

![image](https://github.com/Astryon/Stage2_Final_Project/assets/68798868/d3a1b887-075f-4c90-b0b1-d2a3de885d1b)

6.7. Hasil Datanya : 

![image](https://github.com/Astryon/Stage2_Final_Project/assets/68798868/6e23b50a-4701-42e7-9116-587594fd227b)

## 7. Feature Selection
7.1. Visualisasi Korelasi Data : 

![image](https://github.com/Astryon/Stage2_Final_Project/assets/68798868/ffa529f4-76b3-4434-874f-1ca29c2da9f1)

![image](https://github.com/Astryon/Stage2_Final_Project/assets/68798868/a3d37dbe-9813-4503-8752-b22f7dcc7012)

7.2. Melakukan drop feature yang tidak terpakai atau korelasinya di bawah < 0,1 / -0,1 : 

![image](https://github.com/Astryon/Stage2_Final_Project/assets/68798868/ac0a52da-4755-4cd0-995b-16215e156b1d)

7.3. Melakukan ubah posisi ProdTaken ke paling kanan dan running kembali korelasinya : 

![image](https://github.com/Astryon/Stage2_Final_Project/assets/68798868/20965001-40b4-4645-963a-727f4ebbabc8)

7.4. Melakukan cek kembali 

![image](https://github.com/Astryon/Stage2_Final_Project/assets/68798868/8e500782-b274-4d90-9455-59a78fa13631)

## 8. Splitting Data & Handling Class Imbalance
8.1. Membagi data train dan test (70:30)

![image](https://github.com/Astryon/Stage2_Final_Project/assets/68798868/af9800fc-41f0-4f44-b63d-6529698cd70d)

Didapati nilai baris train set yaitu : 3231 dan nilai untuk baris test set yaitu : 1386 

8.2. Cek fitur train set

![image](https://github.com/Astryon/Stage2_Final_Project/assets/68798868/d4e8a054-f967-4bf6-9845-980d04a2cc49)

8.3. Split x dan y

8.4. Oversampling menggunakan SMOTE, di dapati nilai sebagai berikut : 

![image](https://github.com/Astryon/Stage2_Final_Project/assets/68798868/619e2342-393e-4fa0-a621-b1d4262870f2)

8.5. Berikut untuk jumlah baris train dan test untuk x dan y nya : 

![image](https://github.com/Astryon/Stage2_Final_Project/assets/68798868/037ffecd-b8ef-482a-b0f2-d116458023b5)

# Terima Kasih :) 🐼














