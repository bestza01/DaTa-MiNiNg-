# DaTa-MinNiNg-

โปรเจกต์รวบรวมโค้ดด้าน **Data Mining** สำหรับการเตรียมข้อมูล (Data Preprocessing) การตรวจจับค่าผิดปกติ (Anomaly Detection) และการสร้างโมเดลทำนายผลการคลี่คลายคดีอาชญากรรมด้วย Machine Learning

## ไฟล์ภายในโปรเจกต์
* **`Trainmodel0_1.ipynb`** — วิเคราะห์ข้อมูลคดีฆาตกรรม ทำความสะอาดข้อมูล (จัดการค่าว่างและค่าผิดปกติของอายุ `998`), แปลงข้อมูลเชิงกลุ่มด้วย One-Hot Encoding และเปรียบเทียบประสิทธิภาพโมเดล **Random Forest Classifier** กับ **Decision Tree Classifier** เพื่อทำนายโอกาสการคลี่คลายคดี (`Crime Solved`) รวมถึงแสดงกราฟ Top 10 Feature Importances
* **`สมบัติ_IQR_Anomaly_Detection.ipynb`** — การตรวจจับข้อมูลผิดปกติ (Outlier / Anomaly Detection) ด้วยวิธี Interquartile Range (IQR)

 รุจิภาส สุทธิศักดิ์ 6704800010

## แหล่งที่มาของชุดข้อมูล (Dataset)
* **ชื่อชุดข้อมูล:** Homicide Reports, 1980–2014 (`database.csv`)
* **แหล่งดาวน์โหลด:** [Kaggle - Homicide Reports (Murder Accountability Project)](https://www.kaggle.com/datasets/murderaccountability/homicide-reports)
* **ตัวแปรหลักที่ใช้ในการเทรนโมเดล:**
  * `Victim Age` (อายุของเหยื่อ)
  * `Victim Sex` (เพศของเหยื่อ)
  * `Weapon` (ประเภทอาวุธที่ใช้)
  * `Relationship` (ความสัมพันธ์ระหว่างผู้ก่อเหตุและเหยื่อ)
  * `Crime Solved` (Target: สถานะการคลี่คลายคดี `Yes` / `No`)

## เครื่องมือและไลบรารีที่ใช้
* Python / Google Colab
* Pandas, NumPy
* Scikit-learn (`RandomForestClassifier`, `DecisionTreeClassifier`, `train_test_split`, `classification_report`)
* Matplotlib, Seaborn

## วิธีใช้งาน
1. ดาวน์โหลดไฟล์ `database.csv` จากลิงก์ Kaggle ด้านบน และอัปโหลดเข้าสู่ Google Drive ของตนเอง
2. เปิดไฟล์ `.ipynb` ผ่าน Google Colab
3. ตรวจสอบและแก้ไข Path ของไฟล์ในคำสั่ง `pd.read_csv(...)` ให้ตรงกับตำแหน่งที่เก็บไฟล์ไว้
4. รันโค้ดตามลำดับตั้งแต่เซลล์แรกจนจบ
