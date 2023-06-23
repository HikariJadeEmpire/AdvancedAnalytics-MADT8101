# Customer Single View
:pushpin: **Goal** :fire: : 
> เป้าหมายของเราคือการทำ ```Customer single view``` หรือก็คือการสร้างแผนภาพที่สามารถอธิบายลูกค้า ( customer ) :standing_person: ได้ชัดเจน มี insights :chart_with_upwards_trend: ที่สามารถนำไปวางแผนต่อยอดได้ เช่น การจัดโปรโมชั่นเพื่อการรักษาลูกค้า หรือการทำ Product Recommendation เป็นต้น

#
**Tools & Others**

[![](https://img.shields.io/badge/tools-Power_BI-rgb(244,208,63)?style=f?style=flat-square&logo=powerbi&logoColor=white)](https://app.powerbi.com/)
[![](https://img.shields.io/badge/tools-miro-rgb(244,208,63)?style=f?style=flat-square&logo=miro&logoColor=white)](https://miro.com/)
[![](https://img.shields.io/badge/code-python3.9-green?style=f?style=flat-square&logo=python&logoColor=white&color=2bbc8a)](https://www.python.org/)
[![](https://img.shields.io/badge/tools-jupyter-orange?style=f?style=flat-square&logo=jupyter&logoColor=white)](https://jupyter.org/)
[![](https://img.shields.io/badge/tools-VSCode-blue?style=f?style=flat-square&logo=visualstudiocode&logoColor=white)](https://code.visualstudio.com/)
[![](https://img.shields.io/badge/tools-SkLearn-green?style=f?style=flat-square&logo=scikitlearn&logoColor=white&color=2bbc8a)](https://scikit-learn.org/stable/)
[![](https://img.shields.io/badge/ML-KMeans-green?style=f?style=flat-square&logo=scikitlearn&logoColor=white&color=2bbc8a)](https://scikit-learn.org/stable/)
[![](https://img.shields.io/badge/ML-preprocessing-green?style=f?style=flat-square&logo=scikitlearn&logoColor=white&color=2bbc8a)](https://scikit-learn.org/stable/)
[![](https://img.shields.io/badge/tools-Pandas-green?style=f?style=flat-square&logo=pandas&logoColor=white&color=2bbc8a)](https://pandas.pydata.org/)
[![](https://img.shields.io/badge/tools-Numpy-green?style=f?style=flat-square&logo=numpy&logoColor=white&color=2bbc8a)](https://numpy.org/)
[![](https://img.shields.io/badge/OS-Mac-green?style=f?style=flat-square&logo=macos&logoColor=white)](https://www.apple.com/macos/ventura/)
[![](https://img.shields.io/badge/OS-Windows-green?style=f?style=flat-square&logo=windows&logoColor=white)](https://www.microsoft.com/)
[![](https://img.shields.io/badge/Git_Update-22_Jun_2023-brightgreen?style=f?style=flat-square&logo=github&logoColor=white)](https://github.com/)

#
**Raw data** : <br>

[![](https://img.shields.io/badge/Git-.CSV-rgb(208,211,212)?style=f?style=flat-square&logo=github&logoColor=white)](https://github.com/HikariJadeEmpire/AdvancedAnalytics-MADT8101/blob/main/Week02_CustomerSingleView/supermarket.csv)

*( Supermarket (Lotus) data from 2006 to 2008, US )*

**CODE** : <br>

[![](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/HikariJadeEmpire/AdvancedAnalytics-MADT8101/blob/main/Week02_CustomerSingleView/KMean_LostusAnalytic.ipynb)

# <h4>STEP 1</h4>
> - EDA
> - Clean DATA

First inspection <br>

![outputff](https://github.com/HikariJadeEmpire/AdvancedAnalytics-MADT8101/assets/118663358/f456a7e9-847d-4661-9403-60214cf20f84)

ในภาพด้านบน เป็นการ Plot Histogram ของทุกๆ Features (Columns) เพื่อดูภาพรวมคร่าวๆ หลังจากที่ได้ทำการ Clean DATA :broom: ( e.g. เติมค่า ```NaN``` ) <br>
จะสังเกตเห็นว่า <br>

> - ลูกค้ามักจะมาซื้อสินค้าในช่วงเวลาที่ร้านใกล้จะปิด :no_entry_sign::convenience_store: ( 8pm until close ) มากที่สุด และรองลงมาคือช่วงบ่าย :sun_with_face: ( 1pm - 2pm )
> - โดยส่วนใหญ่ลูกค้าจะซื้อไม่เกิน 10 ชิ้น และมีราคาไม่เกิน  :dollar: 50 US-Dollars
> - ลูกค้าส่วนมากมีรายได้ระดับ :label: MM ( Mid Market ) หรือระดับปานกลาง
> - ช่วงอายุของลูกค้าส่วนใหญ่ระบุไม่ได้ :question: และในส่วนที่ระบุได้ส่วนใหญ่เป็น YF ( Young Families ) :family: 
> - ลูกค้าส่วนมากใช้ตะกร้าขนาดใหญ่ :shopping_cart: ในการเลือกซื้อของ และมักจะซื้อของเต็มตะกร้าเสมอ
> - ลูกค้าโดยส่วนใหญ่ซื้อสินค้าประเภทของสด ( Fresh ) :cut_of_meat:


#
<br>

เพื่อทำให้ได้ตามเป้าหมาย ( [:pushpin: **Goal** :fire:](https://github.com/HikariJadeEmpire/AdvancedAnalytics-MADT8101/blob/main/Week02_CustomerSingleView/week02.md#customer-single-view) ) เราจะนำ ```Analytics Engines``` :gear: มาใช้งาน <br>

จากข้อมูลที่ได้มาในเบื้องต้น สามารถนำมากำหนดเป้าหมาย 	:triangular_flag_on_post: ในการสร้าง ```customer single view``` ได้ ดังแผนภาพด้านล่าง : <br>
<br>

![Personal visualization - cust single view0](https://github.com/HikariJadeEmpire/AdvancedAnalytics-MADT8101/assets/118663358/76e88671-81ff-4350-9f36-fb4262470659)

<br>

**คำอธิบาย :** 
> อ้างอิงจาก Balance contribution ที่มุมบนซ้าย เราได้ตั้งเป้าหมายว่าจะ Focus :triangular_flag_on_post: ไปที่การรักษาลูกค้า <br>
> และนำ ```Analytics Engines``` :gear: มาเรียบเรียงเพื่อดูว่ามีเครื่องมือไหนที่ใช้กับ DATA ชุดนี้ได้บ้าง
>
> จากนั้นก็ทำการ :dart: กำหนดเป้าหมาย แล้วหยิบเอา ```Analytics Engines``` :gear: ที่เหมาะสมมาใช้งาน

<br>
จากแผนภาพดังกล่าว เราสามารถนำ DATA Insights ไปต่อยอดได้ดังตัวอย่างด้านล่างนี้ : <br>
<br>

> 1. กำหนดเวลาในการซื้อสินค้า :soon: โดยใช้ระยะเวลาโปรโมชั่นสั้นๆเพื่อสร้างความคาดหวังและกระตุ้นให้เกิดการซื้อ
> 1. สร้างโปรแกรมสะสมแต้ม :tickets: หรือรางวัลเพื่อกระตุ้นให้เกิดการซื้อซ้ำ
> 1. เสนอของสมนาคุณ :shopping: ต่อผู้ที่มีความสัมพันธ์ที่ดีต่อธุรกิจ เพื่อสร้างความภักดี :muscle:

# <h4>STEP 2</h4>
- DATA Transformation

ในขั้นตอนนี้ เราจะทำการ Transform (ปรับเปลี่ยน) ลักษณะของ Features ให้เหมาะแก่การนำไปใช้งาน <br>
ตามที่ได้กำหนดไว้ในแผนภาพ ซึ่งประกอบไปด้วย *เป้าหมาย* :triangular_flag_on_post: และ ```Analytics Engines``` :gear:  ที่จะนำมาใช้

:white_check_mark: Features Transformation results :

![Personal visualization - Frame 1](https://github.com/HikariJadeEmpire/AdvancedAnalytics-MADT8101/assets/118663358/af0ea13f-89fe-4d00-92ef-f723b86adbe7)

<br>
<br>

ในขั้นตอนต่อจากนี้ จะมีการนำ ```Machine Learning``` เข้ามาช่วย ในการทำ ```Segmentation``` <br>

--------------------------------------

**CODE** : <br>

[![](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/HikariJadeEmpire/AdvancedAnalytics-MADT8101/blob/main/Week02_CustomerSingleView/KMean_LostusAnalytic.ipynb)

--------------------------------------

โดยจะมีขั้นตอนคร่าวๆคือ : <br>

:vertical_traffic_light: **DATA Transformation** by ```preprocessing``` :arrow_forward: **Dimensionality Reduction** By ```TruncatedSVD``` or ```PCA``` :arrow_forward: ```KMeans``` :golfing_man:

ซึ่งจะได้ผลลัพธ์ออกมาเป็น 4 กลุ่ม



#
Go to top : [Top :world_map:](https://github.com/HikariJadeEmpire/AdvancedAnalytics-MADT8101/blob/main/Week02_CustomerSingleView/week02.md#customer-single-view) <br>
Go to home page ( contents ) : 
[Home :earth_asia:](https://github.com/HikariJadeEmpire/AdvancedAnalytics-MADT8101#advancedanalytics-madt8101)

