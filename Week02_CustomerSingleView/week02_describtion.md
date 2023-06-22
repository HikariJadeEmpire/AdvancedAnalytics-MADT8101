# Customer Single View
:pushpin: **Goal** :fire: : 
> เป้าหมายของเราคือการทำ Customer single view หรือก็คือการทำแผนภาพที่สามารถอธิบายลูกค้าได้ชัดเจน มี insights และสามารถนำไปต่อยอดได้

#
**Tools & Others**

[![](https://img.shields.io/badge/tools-miro-green?style=f?style=flat-square&logo=miro&logoColor=white&color=2bbc8a)](https://miro.com/)
[![](https://img.shields.io/badge/code-python3.9-green?style=f?style=flat-square&logo=python&logoColor=white&color=2bbc8a)](https://www.python.org/)
[![](https://img.shields.io/badge/tools-jupyter-orange?style=f?style=flat-square&logo=jupyter&logoColor=white)](https://jupyter.org/)
[![](https://img.shields.io/badge/tools-SkLearn-green?style=f?style=flat-square&logo=scikitlearn&logoColor=white&color=2bbc8a)](https://scikit-learn.org/stable/)
[![](https://img.shields.io/badge/ML-KMeans-green?style=f?style=flat-square&logo=scikitlearn&logoColor=white&color=2bbc8a)](https://scikit-learn.org/stable/)
[![](https://img.shields.io/badge/ML-preprocessing-green?style=f?style=flat-square&logo=scikitlearn&logoColor=white&color=2bbc8a)](https://scikit-learn.org/stable/)
[![](https://img.shields.io/badge/tools-VSCode-blue?style=f?style=flat-square&logo=visualstudiocode&logoColor=white)](https://code.visualstudio.com/)
[![](https://img.shields.io/badge/tools-Pandas-green?style=f?style=flat-square&logo=pandas&logoColor=white&color=2bbc8a)](https://pandas.pydata.org/)
[![](https://img.shields.io/badge/tools-Numpy-green?style=f?style=flat-square&logo=numpy&logoColor=white&color=2bbc8a)](https://numpy.org/)
[![](https://img.shields.io/badge/OS-Mac-green?style=f?style=flat-square&logo=macos&logoColor=white)](https://www.apple.com/macos/ventura/)
[![](https://img.shields.io/badge/OS-Windows-green?style=f?style=flat-square&logo=windows&logoColor=white)](https://www.microsoft.com/)
[![](https://img.shields.io/badge/Git_Update-22_Jun_2023-brightgreen?style=f?style=flat-square&logo=github&logoColor=white)](https://github.com/)

#
**Raw data** : <br>

[![](https://img.shields.io/badge/Git-.CSV-rgb(208,211,212)?style=f?style=flat-square&logo=github&logoColor=white)](https://github.com/HikariJadeEmpire/AdvancedAnalytics-MADT8101/blob/main/Week02_CustomerSingleView/supermarket.csv)

( Supermarket company (Lotus) data from 2006 to 2008 )

**CODE** : <br>

<a href="https://colab.research.google.com/github/HikariJadeEmpire/AdvancedAnalytics-MADT8101/blob/main/Week02_CustomerSingleView/KMean_LostusAnalytic.ipynb"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/>

# <h4>STEP 1</h4>
> - EDA
> - Clean DATA

First inspection <br>

![outputff](https://github.com/HikariJadeEmpire/AdvancedAnalytics-MADT8101/assets/118663358/f456a7e9-847d-4661-9403-60214cf20f84)

ในภาพด้านบน เป็นการ Plot Histogram ของทุกๆ Features (Columns) เพื่อดูภาพรวมคร่าวๆ หลังจากที่ได้ทำการ Clean DATA :broom: ( e.g. เติมค่า ```NaN``` ) <br>
ซึ่งจะสังเกตเห็นว่า <br>

> - ลูกค้ามักจะมาซื้อสินค้าในช่วงเวลาที่ร้านใกล้จะปิด :no_entry_sign::convenience_store: ( 8pm until close ) และ ในช่วงบ่าย :sun_with_face: ( 1pm - 2pm )
> - โดยส่วนใหญ่ลูกค้าจะซื้อไม่เกิน 10 ชิ้น และมีราคาไม่เกิน  :dollar: 50 US-Dollars
> - ลูกค้าส่วนมากมีรายได้ระดับ :label: MM ( Mid Market ) หรือระดับปานกลาง
> - ช่วงอายุของลูกค้าส่วนใหญ่ระบุไม่ได้  :family: และในส่วนที่ระบุได้ส่วนใหญ่เป็น YF ( Young Families )
> - ลูกค้าส่วนมากใช้ตะกร้าขนาดใหญ่ :shopping_cart: ในการเลือกซื้อของ และมักจะ๙ื้อของเต็มตะกร้าเสมอ
> - ลูกค้าโดยส่วนใหญ่ซื้อสินค้าประเภทของสด ( Fresh ) :cut_of_meat:

เพื่อทำให้ได้ตามเป้าหมาย ( [:pushpin: **Goal** :fire:](https://github.com/HikariJadeEmpire/AdvancedAnalytics-MADT8101#advancedanalytics-madt8101) ) เราจะนำ ```Analytics Engines``` มาใช้งาน

#
Go to top : [Top :world_map:](https://github.com/HikariJadeEmpire/AdvancedAnalytics-MADT8101/blob/main/Week02_CustomerSingleView/week02_describtion.md#customer-single-view) <br>
Go to home page ( contents ) : 
[Home :earth_asia:](https://github.com/HikariJadeEmpire/AdvancedAnalytics-MADT8101#advancedanalytics-madt8101)

