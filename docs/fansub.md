# Fansub
แสดงรายชื่อแฟนซับทั้งหมดที่มีในเว็บ TAFASU เหมือนกับ https://www.tafasu.com/fansub

Type | Data
--- | ---
URL | https://www.tafasu.com/api/v1/fansub
HTTP Method | GET
Parameter | name, alias, limit, page, fields
Fields | id, description, alias, facebook, cover, cover, logo
Response | JSON (Array)

## Parameter
Parameter | value
--- | ---
name | ค้นหาโดยชื่อแฟนซับ สามารถใข้ wildcard (%) ได้
alias | ค้นหาโดยชื่อ alias ของแฟนซับ สามารถใข้ wildcard (%) ได้
limit | บอกจำนวนข้อมูลที่จะดึงมาแสดง ตั้งแต่ 0-100 (ค่าเริ่มต้น 10)
page | หน้าข้อมูลปัจจุบัน
fields | ฟิลล์ข้อมูลที่จะนำมาแสดง แบ่งด้วยลูกน้ำ (,)


## Fields
Fields| value
--- | ---
id | รหัสไอดีของแฟนซับนั้น
description | คำโปรยของแฟนซับนั้น
alias | ชื่อแฟนซับสำหรับใช้ใน url ตัวอย่างเช่น www.tafasu.com/fansub/nishikawafs
facebook | url เพจเฟสบุ๊คของแฟนซับนั้นๆ
cover | ภาพพื้นหลังของแฟนซับนั้นๆ
logo | ภาพโลโก้ของแฟนซับนั้นๆ

## ตัวอย่างหน้าที่ใช้ข้อมูลดังกล่าวบนเว็บไซต์ TAFASU
![](/images/preview_fansub.png)

## ตัวอย่าง json
```json
[
  {
    "id": 220,
    "name": "Niceoppai Teamsub",
    "description": "",
    "alias": "niceoppaiteamsub",
    "facebook": "",
    "cover": "",
    "logo": ""
  },
  {
    "id": 90,
    "name": "NishikawaFS",
    "description": "Nishikawa Fansub",
    "alias": "nishikawafs",
    "facebook": "https://www.facebook.com/nishikawafs",
    "cover": "http://i.imgur.com/cVcJTxU.png",
    "logo": "1476027133.png"
  }
]
```
