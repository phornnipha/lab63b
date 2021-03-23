## การทดลองที่ 5 เรื่อง การเขียนโปรแกรมเชื่อมต่อไวไฟและเว็บเซอร์เวอร์

## วัตถุประสงค์
* เพื่อศึกษาการเชื่อมต่อไวไฟและสร้างเว็บเซอร์เวอร์

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
  * [05 run wifi](https://youtu.be/VX-QNQcO-b4)
## วิธีการทำการทดลอง 
1. เริ่มจากการต่อ USB ที่ต่อเชื่อมกับคอมพิวเตอร์ เข้ากับตัว USB to Serial Port

  ![image](https://user-images.githubusercontent.com/80879777/112014167-386fc300-8b5d-11eb-9ae9-118774ac8e2d.png)

2. นำไมโครคอนโทรเลอร์ ( ESP_01 ) ต่อเข้าทาง Serial Port ของตัว USB to Serial Port

  ![image](https://user-images.githubusercontent.com/80879777/112166151-f5c3ee80-8c21-11eb-98d2-86074a7d06be.png)

3. การเปิดโปรแกรม( Command Prompt )ที่จะทำการรัน เข้าโฟลเดอร์ที่บันทึกตัวอย่างโปรแกรมเอาไว้ โดยการทดลองนี้ จะเรียกใช้ตัวอย่างโปรแกรมที่ 05 พิมพ์ **05_Wifi-Wed-Server**  และพิมพ์  **vi src/main.cpp**
  
  ![image](https://user-images.githubusercontent.com/80879777/112186716-fe252500-8c33-11eb-924c-4d2c9402d40f.png)

4. รันคำสั่ง **pio run -t upload** เพื่อที่จะ upload โปรแกรม  05_Wifi-Wed-Serverลงใน ESP_01

  ![image](https://user-images.githubusercontent.com/80879777/112186771-0bdaaa80-8c34-11eb-9e3e-c2e313757c76.png)

5. กดปุ่มสีดำค้างไว้แล้วกดปุ่มแดง(reset) เพื่อให้ ESP_01 รับโปรแกรมใหม่เข้าไป
  
  ![image](https://user-images.githubusercontent.com/80879777/112186804-1432e580-8c34-11eb-8efe-20565f0b94ad.png)

6. เปิด web browser...

********คลิปมีปัญหา******** ******(ไม่ยอมเล่นต่อหลังจากนาทีที่ 2:28)******

   ![image](https://user-images.githubusercontent.com/80879777/112186864-1f861100-8c34-11eb-86d5-511ee4bbf84a.png)

## การบันทึกผลการทดลอง

## อภิปรายผลการทดลอง

## คำถามหลังการทดลอง 
