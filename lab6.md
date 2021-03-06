## การทดลองที่ 6 เรื่อง การเขียนโปรแกรมสร้างไวไฟแอคเซสพอยต์ (Wifi AP)

## วัตถุประสงค์
* เพื่อสร้างสัญญาณไวไฟ โดยใช้ไมโครคอนโทรลเลอร์ที่มีไวไฟในตัวเองในการปล่อยสัญญาณ

## อุปกรณ์ที่ใช้
1.	ไมโครคอนโทรเลอร์ เช่น ESP_01
2.	USB 
3.	USB to Serial Port
4.	อุปกรณ์ที่ใช้ในเขียนโปรแกรม เช่น คอมพิวเตอร์ เป็นต้น
5.	โทรศัพท์มือถือ

## ศึกษาข้อมูลเบื้องต้น
1. การติดตั้งโปรแกรม
   * https://www.youtube.com/watch?v=ocrGdJoP90Y
2. ข้อมูลของไมโครคอนโทรเลอร์
   * [PlatformIO]( https://platformio.org/ )
   * [ESP_01](https://docs.platformio.org/en/latest/boards/espressif8266/esp01_1m.html)

* ตัวอย่างการทำการทดลอง
  * [06 run wiri AP](https://youtu.be/T26DVHePlTs)

## วิธีการทำการทดลอง 
1. เริ่มจากการต่อ USB ที่ต่อเชื่อมกับคอมพิวเตอร์ เข้ากับตัว USB to Serial Port

  ![image](https://user-images.githubusercontent.com/80879777/112014167-386fc300-8b5d-11eb-9ae9-118774ac8e2d.png)

2. นำไมโครคอนโทรเลอร์ ( ESP_01 ) ต่อเข้าทาง Serial Port ของตัว USB to Serial Port

  ![image](https://user-images.githubusercontent.com/80879777/112166151-f5c3ee80-8c21-11eb-98d2-86074a7d06be.png)

3. การเปิดโปรแกรม( Command Prompt )ที่จะทำการรัน เข้าโฟลเดอร์ที่บันทึกตัวอย่างโปรแกรมเอาไว้ โดยการทดลองนี้ จะเรียกใช้ตัวอย่างโปรแกรมที่ 06 พิมพ์ **cd 06_Wifi-AP-Web-Server**  และพิมพ์  **vi src/main.cpp**

  ![image](https://user-images.githubusercontent.com/80879777/112166193-fe1c2980-8c21-11eb-812f-40aeb66d7535.png)

4. รันคำสั่ง **pio run -t upload** เพื่อที่จะ upload โปรแกรม  06_Wifi-AP-Web-Server ลงใน ESP_01

  ![image](https://user-images.githubusercontent.com/80879777/112166245-0a07eb80-8c22-11eb-9bd9-5f512c6e6581.png)

5. กดปุ่มสีดำค้างไว้แล้วกดปุ่มแดง(reset) เพื่อให้ ESP_01 รับโปรแกรมใหม่เข้าไป

  ![image](https://user-images.githubusercontent.com/80879777/112166329-1c822500-8c22-11eb-9574-13bff98dda25.png)

6. รันคำสั่ง pio device monitor เพื่อดูผลที่แสดงผลออกมาบน monitor

  ![image](https://user-images.githubusercontent.com/80879777/112166293-14c28080-8c22-11eb-8b1d-608e5683a920.png)

7. ใช้โทรศัพท์มือถือค้นหาไวไฟ

  ![image](https://user-images.githubusercontent.com/80879777/112166426-31f74f00-8c22-11eb-8b4c-60ee8c48e382.png)

8. บันทึกผลการทดลอง


## การบันทึกผลการทดลอง
* จากการทดลองหลังจากรันคำสั่ง pio device monitor จะเห็นผลที่แสดงออกมาบน monitor จะแสดงผลดังนี้

  ![image](https://user-images.githubusercontent.com/80879777/112166383-2ad04100-8c22-11eb-8790-5fc0b357cb5c.png)

* เมื่อทำการใช้โทรศัพท์มือถือค้นหาไวไฟ จะค้นพบตัวไวไฟตามชื่อที่ตั้งไว้

  ![image](https://user-images.githubusercontent.com/80879777/112166467-3b80b700-8c22-11eb-8ac9-3259afa3d40e.png)

## อภิปรายผลการทดลอง
จากการทดลองที่ 6 เรื่อง การเขียนโปรแกรมสร้างไวไฟแอคเซสพอยต์ (Wifi AP) เราสามารถที่จะเขียนโปรแกรมที่ใช้ในการรันบนไมโครคอนโทรเลอร์ โดยการทดลองเมื่อรันคำสั่งของตัวอย่างที่ 06_Wifi-AP-Web-Server ลงไปบนตัวไมโครคอนโทรเลอร์ ( ESP_01 ) หลังจากรันคำสั่งหมดแล้ว และทำการใช้โทรศัพท์มือถือค้นหาไวไฟ จะค้นพบไวไฟตามชื่อไวไฟตามที่ตั้งไว้คือ **"TUENG-ESP-WIFI"** และมีรหัสคือ **"choompol"**

## คำถามหลังการทดลอง 
  * จากการทดลองที่ 5 และการทดลองนี้ มีความแตกต่างกันอย่างไร
    * ในการทดลองที่ 5 จะต้องทำการเชื่อมต่อไวไฟที่มีอยู่  แต่ในการทดลองนี้ไม่จำเป็นต้องทำการเชื่อมต่อไวไฟไว้
