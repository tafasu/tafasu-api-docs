# Anime Project
อ่านโปรเจคของแฟนซับที่ทำเรื่องนี้ สำหรับหารหัสโปรเจค เพื่อนำไปหาตอนอนิเมะใน /project/:id เป็นลำดับถัดไป

Type | Data
--- | ---
URL | https://www.tafasu.com/api/v1/anime/:alias/projects
HTTP Method | GET
Parameter | limit, page, fields
Fields | id, fansub, fansub.id, fansub.description, fansub.alias, fansub.facebook, fansub.cover, fansub.cover, fansub.logo
Response | JSON (Array)

## Parameter
Parameter | value
--- | ---
limit | บอกจำนวนข้อมูลที่จะดึงมาแสดง ตั้งแต่ 0-100 (ค่าเริ่มต้น 10)
page | หน้าข้อมูลปัจจุบัน
fields | ฟิลล์ข้อมูลที่จะนำมาแสดง แบ่งด้วยลูกน้ำ (,)


## Fields
Fields| value
--- | ---
id | รหัสไอดีของโปรเจคที่แฟนซับทำอยู่ในเรื่องนั้น
fansub | อาเรย์ของรายชื่อแฟนซับที่ทำโปรเจคนั้นอยู่
fansub.id | รหัสไอดีของแฟนซับนั้น
fansub.description | คำโปรยของแฟนซับนั้น
fansub.alias | ชื่อแฟนซับสำหรับใช้ใน url ตัวอย่างเช่น www.tafasu.com/fansub/nishikawafs
fansub.facebook | url เพจเฟสบุ๊คของแฟนซับนั้นๆ
fansub.cover | ภาพพื้นหลังของแฟนซับนั้นๆ
fansub.logo | ภาพโลโก้ของแฟนซับนั้นๆ
status | สถานะของโปรเจคนั้น มี 5 สถานนะได้แก่ (Ongoing,OnHold,Complete,Dropped,Licensed)

## ตัวอย่างหน้าที่ใช้ข้อมูลดังกล่าวบนเว็บไซต์ TAFASU
![](/images/preview_anime_project.png)

## ตัวอย่าง json
```json
[
  {
    "id": 58,
    "fansub": [
      {
        "id": 90,
        "name": "NishikawaFS",
        "description": "Nishikawa Fansub",
        "alias": "nishikawafs",
        "facebook": "https://www.facebook.com/nishikawafs",
        "cover": "http://i.imgur.com/cVcJTxU.png",
        "logo": "1476027133.png"
      }
    ],
    "status": "Ongoing"
  },
  {
    "id": 99,
    "fansub": [
      {
        "id": 128,
        "name": "x105sub",
        "description": "สามารถนำไปแจกจ่ายได้โดยไม่มีเงื่อนไข",
        "alias": "x105sub",
        "facebook": "https://www.facebook.com/259940904122303",
        "cover": "",
        "logo": ""
      }
    ],
    "status": "Ongoing"
  },
  {
    "id": 293,
    "fansub": [
      {
        "id": 96,
        "name": "Oyuji-Fs",
        "description": "เป็นแฟนซับที่ทำทุกอย่างไม่ว่าจะเล่นไพ่ ไฮโล โป๊กเกอร์ แทงม้า เล่นหวย ปล้น เราทำทุกอย่าง ไม่ใช่ล่ะ 5555",
        "alias": "oyujifs",
        "facebook": "https://www.facebook.com/580334005480597",
        "cover": "",
        "logo": "1477928345.png"
      }
    ],
    "status": "Ongoing"
  }
]
```
