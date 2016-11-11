# News
อ่านประกาศทั้งหมดจากระบบ

Type | Data
--- | ---
URL | https://www.tafasu.com/api/v1/news
HTTP Method | GET
Parameter | limit, page, fields
Fields |id, title, poster, view, date
Response | JSON (array)

## Parameter
Parameter | value
--- | ---
limit | บอกจำนวนข้อมูลที่จะดึงมาแสดง ตั้งแต่ 0-100 (ค่าเริ่มต้น 10)
page | หน้าข้อมูลปัจจุบัน
fields | ฟิลล์ข้อมูลที่จะนำมาแสดง แบ่งด้วยลูกน้ำ (,)
## Fields
Fields| value
--- | ---
id | ไอดีของประกาศ
title | หัวเรื่องของประกาศ
poster | ชื่อผู้โพสประกาศ
view | จำนวนครั้งที่ดูประกาศ
date | วันเวลาที่ลงประกาศ


## ตัวอย่างหน้าที่ใช้ข้อมูลดังกล่าวบนเว็บไซต์ TAFASU
![](/images/preview_news.png)

## ตัวอย่าง json
```json
[
  {
    "id": 20,
    "title": "[TAFASU] TAFASU is BETA",
    "poster": "TAFASU",
    "view": "70",
    "date": "2016-11-01T10:04:00+0700"
  }
]
```
