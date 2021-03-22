# การทดลองที่ 2 เรื่อง การเขียนโปรแกรมค้นหาไวไฟ

## วัตถุประสงค์
*  เพื่อให้เข้าใจถึงการเขียนโปรแกรมลงไมโครคอนโทรเลอร์
*  เพื่อให้เข้าใจถึงการเขียนโปรแกรมเพื่อศึกษาการทำงานและการค้นหาไวไฟ


## อุปกรณ์ที่ใช้
1.	ไมโครคอนโทรเลอร์ เช่น ESP_01
2.	USB 
3.	USB to Serial Port
4.	อุปกรณ์ที่ใช้ในเขียนโปรแกรม เช่น คอมพิวเตอร์ เป็นต้น


## ศึกษาข้อมูลเบื้องต้น
*
*

* ตัวอย่างการรัน
  * [02 run example 2](https://youtu.be/yBjab0UNuB8)

## วิธีการทำการทดลอง
1.	เริ่มจากการต่อ USB ที่ต่อเชื่อมกับคอมพิวเตอร์ เข้ากับตัว USB to Serial Port

![image](https://user-images.githubusercontent.com/80879777/112014167-386fc300-8b5d-11eb-9ae9-118774ac8e2d.png)

2.	นำไมโครคอนโทรเลอร์ ( ESP_01 ) ต่อเข้าทาง Serial Port ของตัว USB to Serial Port

![image](https://user-images.githubusercontent.com/80879777/112014545-956b7900-8b5d-11eb-88f4-81741df1817f.png)

3.	ทำการเปิดโปรแกรม( Command Prompt )ที่จะทำการรัน เข้าโฟลเดอร์ที่บันทึกตัวอย่างโปรแกรมเอาไว้ เช่น โฟลเดอร์ชื่อ”Pattani” พิมพ์ **cd Pattani** จะมีตัวอย่างโปรแกรมอยู่ 9 ตัว คือ
   * 01_Serial-Monitor
   * 02_Scan-Wifi
   * 03_Output-Port
   * 04_Input-Port
   * 05_Wifi-Wed-Server
   * 06_Wifi-AP-Web-Server
   * 07_Wed-Server-OnOff
   * 08_MQTT-publish
   * 09_MQTT-subscript

![image](https://user-images.githubusercontent.com/80879777/112014594-a1573b00-8b5d-11eb-9852-1f429a532153.png)

4.	โดยการทดลองนี้ จะเรียกใช้ตัวอย่างโปรแกรมที่ 02 พิมพ์ **cd 02_Scan-Wifi** และพิมพ์  **vi src/main.cpp** โดยมี 2 ส่วน  ส่วนแรก คือส่วน setup() ซึ่งจะ run ครั้งเดียว ซึ่งจะ setup Wifi ให้พร้อมทำงาน และส่วนที่สอง คือส่วน loop() ซึ่งจะ run วนloop ตลอดไป โดยจะแสดงผลว่าเริ่มต้นแกนหา Wifi 

![image](https://user-images.githubusercontent.com/80879777/112027795-20eb0700-8b6a-11eb-9680-f1d147588c67.png)

6.	รันคำสั่ง **pio run -t upload** เพื่อที่จะ upload โปรแกรม  02_Scan-Wifi ลงใน ESP_01

![image](https://user-images.githubusercontent.com/80879777/112027844-2ba59c00-8b6a-11eb-99f6-1d4eb93b41a7.png)

7.	กดปุ่มสีดำค้างไว้แล้วกดปุ่มแดง(reset) เพื่อให้ ESP_01 รับโปรแกรมใหม่เข้าไป

![image](https://user-images.githubusercontent.com/80879777/112027903-3b24e500-8b6a-11eb-9e1e-f3d788a0ef49.png)

8.	รันคำสั่ง **pio device monitor** เพื่อดูผลที่แสดงผลออกมาบนmonitor 

![image](https://user-images.githubusercontent.com/80879777/112027968-4aa42e00-8b6a-11eb-9fd2-526ef0ea893a.png)

9.	ลองกดปุ่มสีแดง(reset) 

![image](https://user-images.githubusercontent.com/80879777/112028022-57288680-8b6a-11eb-976f-8371f0b4f6a6.png)


10.	บันทึกผลการทดลอง

## การบันทึกผลการทดลอง

## อภิปรายผลการทดลอง

## คำถามหลังการทดลอง 
