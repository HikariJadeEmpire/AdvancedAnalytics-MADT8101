# Customer Segmentation
:round_pushpin: **GOAL :fire: :**
> Define customer from raw data using python

# <h4>Tools & Others</h4>

[![](https://img.shields.io/badge/tools-miro-rgb(244,208,63)?style=f?style=flat-square&logo=miro&logoColor=white)](https://miro.com/)
[![](https://img.shields.io/badge/code-python3.10-green?style=f?style=flat-square&logo=python&logoColor=white&color=2bbc8a)](https://www.python.org/)
[![](https://img.shields.io/badge/tools-jupyter-orange?style=f?style=flat-square&logo=jupyter&logoColor=white)](https://jupyter.org/)
[![](https://img.shields.io/badge/tools-VSCode-blue?style=f?style=flat-square&logo=visualstudiocode&logoColor=white)](https://code.visualstudio.com/)
[![](https://img.shields.io/badge/tools-Pandas-green?style=f?style=flat-square&logo=pandas&logoColor=white&color=2bbc8a)](https://pandas.pydata.org/)
[![](https://img.shields.io/badge/tools-SkLearn-green?style=f?style=flat-square&logo=scikitlearn&logoColor=white&color=2bbc8a)](https://scikit-learn.org/stable/)
[![](https://img.shields.io/badge/ML-GaussianMixture-green?style=f?style=flat-square&logo=scikitlearn&logoColor=white&color=2bbc8a)](https://scikit-learn.org/stable/)
[![](https://img.shields.io/badge/OS-Mac-green?style=f?style=flat-square&logo=macos&logoColor=white)](https://www.apple.com/macos/ventura/)
[![](https://img.shields.io/badge/OS-Windows-green?style=f?style=flat-square&logo=windows&logoColor=white)](https://www.microsoft.com/)
[![](https://img.shields.io/badge/Git_Update-12_Jul_2023-brightgreen?style=f?style=flat-square&logo=github&logoColor=white)](https://github.com/)

#
**Raw data** : <br>

[![](https://img.shields.io/badge/Git-.CSV-rgb(208,211,212)?style=f?style=flat-square&logo=github&logoColor=white)](https://github.com/HikariJadeEmpire/AdvancedAnalytics-MADT8101/blob/main/Section04/Week05_CustomerSegmentation/WEEK05_AdvancedAnalytics.zip)

*( RESTRICTED : MLM (Multi-Level Marketing) or Network Marketing data from 2021 to 2023 )*

**CODE** : <br>

[![](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/HikariJadeEmpire/AdvancedAnalytics-MADT8101/blob/main/Section04/Week05_CustomerSegmentation/week5-Segmentation.ipynb)

#

:mag: **1st Inspection** <br>
After cleaning the data, I take another step to define customer behavior and perform segmentation. <br>

Criteria of selecting customer behavior : 
- RFM ( Recency Frequency Monetary ) analysis or RFM segmentation.

So, I need to transform the data from simple to RFM data.

![Personal visualization - Frame 3](https://github.com/HikariJadeEmpire/AdvancedAnalytics-MADT8101/assets/118663358/7efb599c-981c-4f88-8676-770a4e0c10a2)

The next step is to perform segmentation using these columns as follows

![Personal visualization - Frame 4](https://github.com/HikariJadeEmpire/AdvancedAnalytics-MADT8101/assets/118663358/f091c9c0-cb61-4522-a04c-c43d5352bcc8)


# <h3>Segmentation result</h3>

- Overall (Segment 01)

![output1-0](https://github.com/HikariJadeEmpire/AdvancedAnalytics-MADT8101/assets/118663358/6ef1ffb0-4f00-4f03-9e66-4aba67a5ed5f)


- Last 6 month (Segment 02)

![output1-6m](https://github.com/HikariJadeEmpire/AdvancedAnalytics-MADT8101/assets/118663358/01d81b5b-ee93-4827-a935-1707f22b8fa5)

  
- Last 3 month (Segment 03)

![output1-3m](https://github.com/HikariJadeEmpire/AdvancedAnalytics-MADT8101/assets/118663358/f8468d9d-78e1-4ea0-bae8-96ca3804a8db)

<br>

<h3>Feature Importance</h3>

Overall (Segment 01)
> **Cluster 0 :** Total Spending , Total Network (Tier 1)<br>
> **Cluster 1 :** Total Spending , Total Network (Tier 2) <br>
> **Cluster 2 :** Total Spending , Member Duration , Total Network <br>
> **Cluster 3 :** Total Spending , Total Transaction , Total Network <br>
> **Cluster 4 :** Total Network , Member Duration , Total Spending , Ticket Size <br>
> **Cluster 5 :** Total Spending , Total Network (Tier 3)

Last 6 month (Segment 02)
> **Cluster 0 :** SKU last 6m , Network last 6m <br>
> **Cluster 1 :** Spending last 6m online , Transaction last 6m <br>
> **Cluster 2 :** Spending last 6m , Member Duration <br>
> **Cluster 3 :** Spending last 6m , Transaction last 6m <br>
> **Cluster 4 :** Spending last 6m online , Spending last 6m offline , Network last 6m <br>
> **Cluster 5 :** Spending last 6m offline , Spending last 6m online <br>

Last 3 month (Segment 03)
> **Cluster 0 :** Transaction last 3m , Network last 3m <br>
> **Cluster 1 :** Spending last 3m , Transaction last 3m <br>
> **Cluster 2 :** Spending last 3m , Spending last 3m offline , Spending last 3m online <br>
> **Cluster 3 :** Spending last 3m offline , Spending last 3m online <br>
> **Cluster 4 :** Spending last 3m online , Spending last 3m offline , Network last 3m <br>
> **Cluster 5 :** Spending last 3m , Transaction last 3m , Spending last 3m online <br>

# <h3>Segmentation Movement</h3>

![newplot0](https://github.com/HikariJadeEmpire/AdvancedAnalytics-MADT8101/assets/118663358/191b6e96-919d-490d-a3c4-07932537a5bd)

#
Go to top : [Top :world_map:](https://github.com/HikariJadeEmpire/AdvancedAnalytics-MADT8101/blob/main/Section04/Week05_CustomerSegmentation/week05.md#customer-segmentation) <br>
Go to home page ( contents ) : 
[Home :earth_asia:](https://github.com/HikariJadeEmpire/AdvancedAnalytics-MADT8101#advancedanalytics-madt8101)
