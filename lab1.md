# การทดลองที่ 1 เรื่อง การเขียนโปรแกรมเพื่อรันบนไมโครคอนโทรเลอร์

## วัตถุประสงค์
*  เพื่อให้ศึกษาและเข้าใจถึงการเขียนโปรแกรมที่ใช้ในการรันคำสั่งบนไมโครคอนโทรเลอร์

## อุปกรณ์ที่ใช้
1.	ไมโครคอนโทรเลอร์ เช่น ESP_01
2.	USB 
3.	USB to Serial Port
4.	อุปกรณ์ที่ใช้ในเขียนโปรแกรม เช่น คอมพิวเตอร์ เป็นต้น


## ศึกษาข้อมูลเบื้องต้น
1. การติดตั้งโปรแกรม
   * https://www.youtube.com/watch?v=ocrGdJoP90Y
2. ข้อมูลของไมโครคอนโทรเลอร์
   * [PlatformIO]( https://platformio.org/ )
   * [ESP_01](https://docs.platformio.org/en/latest/boards/espressif8266/esp01_1m.html)

* ตัวอย่างการทำการทดลอง
  * [01 run example 1](https://www.youtube.com/watch?v=NLIUsWLEpmg)

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

4.	โดยการทดลองนี้ จะเรียกใช้ตัวอย่างโปรแกรมที่ 01 พิมพ์ **cd 01_Serial-Monitor**  

![image](https://user-images.githubusercontent.com/80879777/112015843-c4361f00-8b5e-11eb-9a6f-513499bb1e4c.png)
https://github.com/phornnipha/lab1/blob/main/IMG_0631.PNG

5.	พิมพ์  **vi src/main.cpp** ซึ่งเป็นโปรแกรมที่เขียนขึ้นมาเพื่อทดสอบไมโครคอนโทรเลอร์ ซึ่งมีอยู่ 15 บรรทัด มี 2 ส่วนโดย เขียนด้วยภาษา C หรือ C++ ส่วนแรก คือส่วน setup() ซึ่งจะ run ครั้งเดียว ซึ่งจะ set serial Port ที่ความเร็ว 115200 และส่วนที่สอง คือส่วน loop() ซึ่งจะ run วนloop ตลอดไป 

![image](https://user-images.githubusercontent.com/80879777/112015929-d57f2b80-8b5e-11eb-9a00-468f7406caff.png)

6.	ในแต่ละโปรแกรมที่ใช้ platformio จะมี confituration file ชื่อว่า platformio.ini ซึ่งจะบอกว่าเป็น platform ของบริษัทอะไร board ชื่ออะไร ใช้วิธีเขียนโปรแกรมแบบไหน port ที่ใช้ติดต่อกับคอมใช้อะไร โดยจะพิมพ์**vi  platformio.ini**

![image](https://user-images.githubusercontent.com/80879777/112015978-e0d25700-8b5e-11eb-83b9-08c8fe096d8e.png)

7.	รันคำสั่ง **pio run -t upload** เพื่อที่จะ upload โปรแกรม 01_Serial-Monitor ลงใน ESP_01

![image](https://user-images.githubusercontent.com/80879777/112016021-e92a9200-8b5e-11eb-868c-be2d541fc1d1.png)

8.	กดปุ่มสีดำค้างไว้แล้วกดปุ่มแดง(reset) เพื่อให้ ESP_01 รับโปรแกรมใหม่เข้าไป

![image](https://user-images.githubusercontent.com/80879777/112016079-f5165400-8b5e-11eb-9bca-57a5a741b16b.png)

9.	รันคำสั่ง **pio device monitor** เพื่อดูผลที่แสดงผลออกมาบนmonitor 

![image](https://user-images.githubusercontent.com/80879777/112016134-04959d00-8b5f-11eb-8169-3b7e60e7030a.png)

10.	ลองกดปุ่มสีแดง(reset) 

![image](https://user-images.githubusercontent.com/80879777/112016236-2131d500-8b5f-11eb-8652-bdab24a92468.png)

11.บันทึกผลการทดลอง


## การบันทึกผลการทดลอง
* จากการทดลองจะเห็นผลที่แสดงผลออกมาบนmonitor เป็นตัวเลขที่เพิ่มขึ้นทีละ 1 ในทุกๆ 1s(1000ms) ไปเรื่อยๆ

![image](https://user-images.githubusercontent.com/80879777/112017409-2cd1cb80-8b60-11eb-96b9-210df46bdaee.png)

* เมื่อกดปุ่มสีแดง(reset) ค่าจะถูก reset และเริ่มใหม่จาก 1 และเพิ่มขึ้นทีละ 1 ในทุกๆ 1s แบบเดิม 

![image](https://user-images.githubusercontent.com/80879777/112017353-1deb1900-8b60-11eb-811a-ee6d48160a2b.png)

## อภิปรายผลการทดลอง
   *     จากการทดลองที่ 1 เรื่อง การเขียนโปรแกรมเพื่อรันบนไมโครคอนโทรเลอร์ เราสามารถที่จะเขียนโปรแกรมที่ใช้ในการรันบนไมโครคอนโทรเลอร์ โดยการทดลองนี้เมื่อรันคำสั่งของตัวอย่างที่ 01_Serial-Monitor ลงไปบนตัวไมโครคอนโทรเลอร์ ( ESP_01 ) หลังจากรันคำสั่งหมดแล้ว ตัวโปรแกรมจะทำการนับเลขเพิ่มขึ้นทีละ 1 ในทุกๆ 1s ไปเรื่อยๆ จนกว่าจะกดปุ่มสีแดง(reset) ตัวไมโครคอนโทรเลอร์จะ  reset และเริ่มใหม่จาก 1 และเพิ่มขึ้นทีละ 1 ในทุกๆ 1s แบบเดิม 

## คำถามหลังการทดลอง 
   * จากการทดลองนี้ ถ้าต้องเปลี่ยนผลการรันที่จะเเสดงผลออกมาบน monitor ให้เปลี่ยนแปลงไป จะต้องเปลี่ยนการเขียนโปรแกรมส่วนใด
     * เราจะสามารถที่จะเขียนโปรแกรม โดยการเปลี่ยนในส่วนของ **loob**  เพื่อให้ได้การทำงานตามที่ต้องการได้ 
   
   

