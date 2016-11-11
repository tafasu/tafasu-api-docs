# Fansub Data
อ่านข้อมูลของแฟนซับที่กำหนด โดยใช้ alias หรือ id ตัวอย่างเช่น  https://www.tafasu.com/api/v1/fansub/nishikawafs หรือ https://www.tafasu.com/api/v1/fansub/90 จะได้ข้อมูลแฟนซับของ NishikawaFS กลับมา

Type | Data
--- | ---
URL | https://www.tafasu.com/api/v1/fansub/:alias
HTTP Method | GET
Parameter | fields
Fields | id, name, alias, description, facebook, cover, logo
Response | JSON (object)

## Parameter
Parameter | value
--- | ---
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
![](/images/preview-anime-alias.png)

## ตัวอย่าง json
```json
{
  "id": 90,
  "name": "NishikawaFS",
  "description": "Nishikawa Fansub",
  "alias": "nishikawafs",
  "facebook": "https://www.facebook.com/nishikawafs",
  "cover": "http://i.imgur.com/cVcJTxU.png",
  "logo": "1476027133.png"
}
```
