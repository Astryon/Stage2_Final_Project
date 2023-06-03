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

