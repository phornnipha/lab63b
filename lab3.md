# การทดลองที่ 3 เรื่อง การเขียนโปรแกรมเอ้าต์พุทสัญญาณดิจิทัล
## วัตถุประสงค์
*  เพื่อเขียนโปรแกรมลงไมโครคอนโทรเลอร์และการนำเอ้าต์พุทไปใช้งานกับอุปกรณ์อื่น
## อุปกรณ์ที่ใช้
1.	ไมโครคอนโทรเลอร์ เช่น  ESP_01
2.	USB
3.	อุปกรณ์ต่อ USB to Serial Port
4.	อุปกรณ์ที่ใช้ในเขียนโปรแกรม เช่น คอมพิวเตอร์ เป็นต้น
5.	Adapter
6.	หลอด LED 
7.	Relay
## ศึกษาข้อมูลเบื้องต้น

## วิธีการทำการทดลอง 
* ตอนที่ 1
  1.	เริ่มจากการต่อ USB ที่ต่อเชื่อมกับคอมพิวเตอร์ เข้ากับตัว USB to Serial Port

  ![image](https://user-images.githubusercontent.com/80879777/112014167-386fc300-8b5d-11eb-9ae9-118774ac8e2d.png)

  2.	นำ Adapterต่อเข้าทาง Serial Port
  
  ![image](https://user-images.githubusercontent.com/80879777/112043443-43d1e700-8b7b-11eb-983a-67b0a39824c3.png)

  3.	นำ ไมโครคอนโทรเลอร์ (ESP_01) ต่อเข้ากับ Serial Port ของ Adapter
  ![image](https://user-images.githubusercontent.com/80879777/112043502-50eed600-8b7b-11eb-883c-053317478ee0.png)
  
  4.ต่อหลอด LED ที่พอต 0 และ 2
  
  ![image](https://user-images.githubusercontent.com/80879777/112045429-6d8c0d80-8b7d-11eb-9155-62dc70fcf070.png)

  5..	ทำการเปิดโปรแกรม( Command Prompt )ที่จะทำการรัน เข้าโฟลเดอร์ที่บันทึกตัวอย่างโปรแกรมเอาไว้ โดยการทดลองนี้ จะเรียกใช้ตัวอย่างโปรแกรมที่ 03 พิมพ์ **03_Output-Port**  และพิมพ์  **vi src/main.cpp** 

  ![image](https://user-images.githubusercontent.com/80879777/112043570-6401a600-8b7b-11eb-913a-958bfed148ed.png)

  6.	รันคำสั่ง *pio run -t upload* เพื่อที่จะ upload โปรแกรม  03_Output-Port ลงใน ESP_01
  ![image](https://user-images.githubusercontent.com/80879777/112043628-74b21c00-8b7b-11eb-9ba7-3e4d8d19322f.png)

  7.	กดปุ่มดำค้างไว้แล้วกดปุ่ม reset เพื่อให้ ESP_01 รับโปรแกรมใหม่เข้าไป 
   ![image](https://user-images.githubusercontent.com/80879777/112043717-8b587300-8b7b-11eb-9eb9-0be349803367.png)

  8.	รันคำสั่ง* pio device monitor* เพื่อดูผลที่แสดงผลออกมาบนmonitor 
 ![image](https://user-images.githubusercontent.com/80879777/112044148-0d489c00-8b7c-11eb-9972-af6d2d9169d4.png)

  9.	ลองกดปุ่มสีแดง(reset)
 
* ตอนที่ 2
  1.	ถอดไมโครคอนโทรเลอร์ (ESP_01) ออกจาก Serial Port ของ Adapter แล้วนำไปต่อกับ Serial Port ของ Relay พร้อมต่อไฟ 5 V เข้า Relay
![image](https://user-images.githubusercontent.com/80879777/112044717-b8f1ec00-8b7c-11eb-809b-b22ddb80d42b.png)

*บันทึกผลการทดลอง


## การบันทึกผลการทดลอง
* ตอนที่ 1


## อภิปรายผลการทดลอง

## คำถามหลังการทดลอง 
