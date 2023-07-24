# Churn Scoring
:round_pushpin: **GOAL :fire: :**
> Define customer churn :running: from raw data using python

# <h4>Tools & Others</h4>

[![](https://img.shields.io/badge/code-python3.10-green?style=f?style=flat-square&logo=python&logoColor=white&color=2bbc8a)](https://www.python.org/)
[![](https://img.shields.io/badge/tools-jupyter-orange?style=f?style=flat-square&logo=jupyter&logoColor=white)](https://jupyter.org/)
[![](https://img.shields.io/badge/tools-VSCode-blue?style=f?style=flat-square&logo=visualstudiocode&logoColor=white)](https://code.visualstudio.com/)
[![](https://img.shields.io/badge/tools-Pandas-green?style=f?style=flat-square&logo=pandas&logoColor=white&color=2bbc8a)](https://pandas.pydata.org/)
[![](https://img.shields.io/badge/OS-Mac-green?style=f?style=flat-square&logo=macos&logoColor=white)](https://www.apple.com/macos/ventura/)
[![](https://img.shields.io/badge/OS-Windows-green?style=f?style=flat-square&logo=windows&logoColor=white)](https://www.microsoft.com/)
[![](https://img.shields.io/badge/Git_Update-5_Jul_2023-brightgreen?style=f?style=flat-square&logo=github&logoColor=white)](https://github.com/)

#
**Raw data** : <br>

[![](https://img.shields.io/badge/Git-.CSV-rgb(208,211,212)?style=f?style=flat-square&logo=github&logoColor=white)](https://github.com/HikariJadeEmpire/AdvancedAnalytics-MADT8101/blob/main/Week02_CustomerSingleView/supermarket.csv)

*( Supermarket (Lotus) data from 2006 to 2008, US )*

**CODE** : <br>

[![](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/HikariJadeEmpire/AdvancedAnalytics-MADT8101/blob/main/Week04_ChurnScoring/myChurnPrediction.ipynb)

#

:mag: **1st Inspection of CHURN** <br>

*(The data remains the same as in [Section01.](https://github.com/HikariJadeEmpire/AdvancedAnalytics-MADT8101/blob/main/Week02_CustomerSingleView/week02.md#customer-single-view))*

- Using Cohort Analysis

<br>

![outputChurn0](https://github.com/HikariJadeEmpire/AdvancedAnalytics-MADT8101/assets/118663358/a81cbcf5-828f-421a-90fc-1dfecfa7ef2b)

<br>

In order to define :running: churn customers, I will create an indicator that facilitates a clearer understanding as follows :

<br>

```ruby

CHURN_Score = [(number of months since registeration)-(active_count)]/(number of months since registeration)

```
<br>

As evident from the table presented below: <br>

<br>

<img width="793" alt="Screenshot 2566-07-22 at 19 11 34" src="https://github.com/HikariJadeEmpire/AdvancedAnalytics-MADT8101/assets/118663358/26d93885-6c81-4af6-ab2e-25f11ac3ba81">

<br>
<br>

In order to enhance comprehension, I will construct a comprehensive graph below :

<br>

![churn](https://github.com/HikariJadeEmpire/AdvancedAnalytics-MADT8101/assets/118663358/f5c2f1cc-8f2b-4dc5-a75e-4e910a781823)

#
Go to top : [Top :world_map:](https://github.com/HikariJadeEmpire/AdvancedAnalytics-MADT8101/blob/main/Section03/Week04_ChurnScoring/week04.md#churn-scoring) <br>
Go to home page ( contents ) : 
[Home :earth_asia:](https://github.com/HikariJadeEmpire/AdvancedAnalytics-MADT8101#advancedanalytics)
