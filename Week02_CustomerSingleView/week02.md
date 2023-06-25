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

![Personal visualization - Frame 1](https://github.com/HikariJadeEmpire/AdvancedAnalytics-MADT8101/assets/118663358/6f15bccd-c8d3-421b-adff-8c3230c6b607)


<br>
<br>

ในขั้นตอนต่อจากนี้ จะมีการนำ ```Machine Learning``` เข้ามาช่วย ในการทำ ```Segmentation``` <br>

--------------------------------------

**CODE** : <br>

[![](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/HikariJadeEmpire/AdvancedAnalytics-MADT8101/blob/main/Week02_CustomerSingleView/KMean_LostusAnalytic.ipynb)

--------------------------------------

โดยจะมีขั้นตอนคร่าวๆคือ : <br>

:vertical_traffic_light: **DATA Transformation** by ```preprocessing``` :arrow_forward: **Dimensionality Reduction** By ```TruncatedSVD``` or ```PCA``` :arrow_forward: ```KMeans``` :golfing_man:

ซึ่งจะได้ผลลัพธ์ออกมาเป็น 4 กลุ่ม <br>
โดยเราจะทำการไล่เรียงลำดับจาก the worst :arrow_forward: the best <br>

ซึ่งจะเริ่มจากกลุ่มที่ 0

![lot00_Page_1](https://github.com/HikariJadeEmpire/AdvancedAnalytics-MADT8101/assets/118663358/b7495434-a86b-494d-ac72-0b2454302d0d)


สำหรับกลุ่มนี้ จะมีลักษณะคือ :
> 1. มักจะใช้ตะกร้า size S และซื้อไม่เต็มตะกร้า (โดยส่วนมาก)
> 2. Life stage : OT (Others) or OA (Old Adult) โดยภาพรวมแล้วค่อนข้างที่จะหลากหลาย
> 3. มักจะมาซื้อสินค้าในช่วงวันจันทร์ เวลา 9pm
> 4. มักจะซื้อสินค้าประเภทของสด :cut_of_meat: และรองลงมาคือสินค้าประเภท Grocery
> 5. โดยรวมแล้วกลุ่มนี้มีการซื้อสินค้าเฉลี่ยต่อปีน้อยที่สุด

กลุ่มถัดมาคือกลุ่มที่ 3

![lot01_Page_1](https://github.com/HikariJadeEmpire/AdvancedAnalytics-MADT8101/assets/118663358/92fc9912-a63f-4ce9-8704-6c1c4c52d89f)


สำหรับกลุ่มนี้ จะมีลักษณะคือ :
> 1. มักจะใช้ตะกร้า size M และซื้อไม่เต็มตะกร้า
> 2. Life stage : Mixed หรือ หลากหลายช่วงอายุ
> 3. มักจะมาซื้อสินค้าในช่วงวันอาทิตย์ เวลา 1pm
> 4. โดยรวมแล้วกลุ่มนี้จะมีการซื้อสินค้าเฉลี่ยต่อปีมากกว่ากลุ่มก่อนหน้านิดหน่อย (ไม่ต่างกันมาก)

กลุ่มถัดมาคือกลุ่มที่ 1

![lotusReport pdf_Page_1](https://github.com/HikariJadeEmpire/AdvancedAnalytics-MADT8101/assets/118663358/6e91036d-f0f8-4706-a181-259d3ced6488)


สำหรับกลุ่มนี้ จะมีลักษณะคือ :
> 1. มักจะใช้ตะกร้า size L และซื้อเต็มตะกร้า
> 2. Life stage : OT (Others) or YF (Young Family)
> 3. มักจะมาซื้อสินค้ามากที่สุดในตอนบ่าย (1pm) และเวลา 9pm ในวันจันทร์ และ วันศุกร์
> 4. มักจะซื้อสินค้าในระดับราคา ต่ำ-ปานกลาง
> 5. มักจะซื้อสินค้าประเภท Mixed หรือซื้อของหลากหลายประเภทรวมกัน
> 6. โดยรวมแล้วกลุ่มนี้จะมีการซื้อสินค้าเฉลี่ยต่อปีค่อนข้างสูง

กลุ่มถัดมาคือกลุ่มที่ 2 (กลุ่มสุดท้าย) <br>

![lotusReport pdf2_Page_1](https://github.com/HikariJadeEmpire/AdvancedAnalytics-MADT8101/assets/118663358/362d4366-eaca-461b-8fae-5278a72b706e)


สำหรับกลุ่มนี้ จะมีลักษณะคือ :
> 1. มักจะใช้ตะกร้า size L และซื้อล้นตะกร้า
> 2. SKU Penetrate โดยเฉลี่ยสูงที่สุด หรือมีการซื้อสินค้าโดยเฉลี่ยแทบจะครบทุกประเภทในร้าน
> 3. Life stage : XX หรือ ไม่สามารถระบุได้
> 5. มักจะมาซื้อสินค้าในช่วงวันอังคาร เวลา 9pm
> 7. มักจะซื้อสินค้าในระดับราคา ปานกลาง-สูง
> 8. มักจะซื้อสินค้าประเภทของสด :cut_of_meat:
> 11. โดยรวมแล้วกลุ่มนี้จะมีการซื้อสินค้าเฉลี่ยต่อปีสูงที่สุด

<br>

# RESULTS

จากนั้นเราจะทำการเปรียบเทียบ ( Comparing ) แต่ละ Cluster เพื่ออธิบายลักษณะของแต่ละกลุ่ม

![lotusReport pdf_Page_2](https://github.com/HikariJadeEmpire/AdvancedAnalytics-MADT8101/assets/118663358/95bad78b-460b-45d0-9c76-8adf42f3e647)

<br>

สำหรับการเปรียบเทียบ Cluster แต่ละกลุ่ม เราจะทำการเรียงลำดับตามอัตราการซื้อสินค้าจาก น้อย-มาก พบว่า :

1. กลุ่ม 0 :purple_circle: (สีม่วง) คือกลุ่มที่มักจะซื้อสินค้าประเภทของชำ และสินค้าประเภทที่ :x: ไม่ใช่อาหาร ซึ่งมักจะซื้อในจำนวนที่น้อย ไม่หลากหลาย แต่มาซื้อบ่อย
2. กลุ่ม 3 :large_orange_diamond: ( สีส้ม ) คือกลุ่มที่มักจะมีค่าที่เป็น XX คือระบุไม่ได้ :grey_question: และเป็นคนกลุ่มน้อย มาไม่บ่อย แต่ซื้อเยอะกว่ากลุ่ม 0 :large_blue_circle:
3. กลุ่ม 1 :large_blue_diamond: ( สีน้ำเงินเข้ม ) คือกลุ่มที่มาไม่บ่อย แต่เมื่อมาแล้วมักจะซื้อของหลายอย่าง และซื้อเยอะเต็มตะกร้า :shopping: และเป็นกลุ่มที่ชอบซื้อของราคาถูก :label:
4. กลุ่ม 2 :large_blue_circle: ( สีฟ้า ) คือกลุ่มที่ซื้อของแพง :gem: ซื้อเยอะที่สุด และซื้อบ่อย มักจะซื้อสินค้าประเภทของสด :cut_of_meat:

<br>

เมื่อสังเกตลักษณะของกลุ่มลูกค้าทั้ง 4 กลุ่มแล้ว เราจะทำการสุ่มตัวอย่างลูกค้าขึ้นมา 1 คน <br>
เพื่อนำมาเป็นตัวอย่างของ Customer single view <br>

![Personal visualization - cust single view1](https://github.com/HikariJadeEmpire/AdvancedAnalytics-MADT8101/assets/118663358/6cdd578d-29a3-473d-ab93-f589afcbafee)

<br>
เราสามารถนำข้อมูลที่ได้มา เพื่อทำตามเป้าหมายที่ตั้งไว้ในตอนเริ่มต้น ซึ่งก็คือการ <br>

:crayon: **Design loyalty tiers** and :rocket: actions follow their spending styles. :money_with_wings:

ซึ่งเราสามารถคิด Campaign เพื่อการเสนอเจาะจงเป็นรายบุคคล :bust_in_silhouette: ก็ได้ หรือจะเป็นรายกลุ่ม :family_man_woman_girl_boy: ก็ได้

# Actions

ในกรณีตัวอย่างที่นำมาแสดง หากเราจะทำการ Design Campaign เพื่อการรักษาลูกค้าในกลุ่มที่ 1 :large_blue_diamond: ( สีน้ำเงินเข้ม ) เราอาจจะเริ่มที่ <br>
- การจัด Promotion ซื้อ 1 แถม 1 หรือ :red_envelope: เสนอสินค้าที่ซื้อคู่กันแล้วได้ส่วนลด โดยจะจัดเฉพาะในวันเสาร์ - อาทิตย์ เพื่อดึงดูดให้ลูกค้ากลุ่มนี้มา Shopping :shopping_cart: บ่อยขึ้น เป็นต้น

#
Go to top : [Top :world_map:](https://github.com/HikariJadeEmpire/AdvancedAnalytics-MADT8101/blob/main/Week02_CustomerSingleView/week02.md#customer-single-view) <br>
Go to home page ( contents ) : 
[Home :earth_asia:](https://github.com/HikariJadeEmpire/AdvancedAnalytics-MADT8101#advancedanalytics-madt8101)

