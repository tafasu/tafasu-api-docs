#Project Episode
อ่านตอนของอนิเมะที่อยู่ในโปรเจคที่กำหนด

Type | Data
--- | ---
URL | https://www.tafasu.com/api/v1/news
HTTP Method | GET
Parameter | limit, page, fields
Fields | hash, name, url, type, view, date, publish
Response | JSON (Array)

## Parameter
Parameter | value
--- | ---
fields | ฟิลล์ข้อมูลที่จะนำมาแสดง แบ่งด้วยลูกน้ำ (,)
## Fields
Fields| value
--- | ---
hash | ค่า hash ของอนิเมะตอนนั้น สำหรับใช้เรียกข้อมูลผ่าน /watch
name | ชื่อตอน
url | url สำหรับดู
type | ประเภทของตอนนั้น มีด้วยกันทั้งสิ้น 7 ประเภทได้แก่ episode, ova, oad, movie, sp ,pv ,ona
view | จำนวนคนดู
date | วันที่โพส
publish | แสดงใน /anime/recent หรือไม่ (true/false)


## ตัวอย่างหน้าที่ใช้ข้อมูลดังกล่าวบนเว็บไซต์ TAFASU
![](/images/preview_project_episode.png)

## ตัวอย่าง json
```json
[
  {
    "hash": "97UNWyHIMz",
    "name": "03",
    "url": "https://www.tafasu.com/watch?v=97UNWyHIMz",
    "type": "episode",
    "view": 101,
    "date": "23/10",
    "publish": true
  },
  {
    "hash": "ybeKBjlvot",
    "name": "02",
    "url": "https://www.tafasu.com/watch?v=ybeKBjlvot",
    "type": "episode",
    "view": 108,
    "date": "23/10",
    "publish": true
  },
  {
    "hash": "6n48CuifRW",
    "name": "01",
    "url": "https://www.tafasu.com/watch?v=6n48CuifRW",
    "type": "episode",
    "view": 143,
    "date": "23/10",
    "publish": false
  }
]
```
