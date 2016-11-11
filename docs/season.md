# Season
อ่านปรานชื่อซีซั่นทั้งหมด

Type | Data
--- | ---
URL | https://www.tafasu.com/api/v1/season
HTTP Method | GET
Parameter | limit, page, fields, id, name
Fields |id, year, name,
Response | JSON (array)

## Parameter
Parameter | value
--- | ---
limit | บอกจำนวนข้อมูลที่จะดึงมาแสดง ตั้งแต่ 0-100 (ค่าเริ่มต้น 10)
page | หน้าข้อมูลปัจจุบัน
fields | ฟิลล์ข้อมูลที่จะนำมาแสดง แบ่งด้วยลูกน้ำ (,)
id | แสดงข้อมูลซีซั่นของไอดีที่กำหนด
name | แสดงข้อมูลซีซันโดยชื่อ โดยใช้ ชื่อซีซั่นติดกับปี เช่น ?name=fall2016 เป็นต้น

## Fields
Fields| value
--- | ---
id | ไอดีของซีซั่น
year | ปีของซีซัน
ืname | ชื่อของซีซั่น ได้แก่ Spring Summer Fall Winter


## ตัวอย่างหน้าที่ใช้ข้อมูลดังกล่าวบนเว็บไซต์ TAFASU
![](/images/preview_season.png)

## ตัวอย่าง json
```json
[
  {
    "id": 1,
    "year": "2016",
    "name": "Fall"
  },
  {
    "id": 10,
    "year": "2016",
    "name": "Summer"
  },
  {
    "id": 23,
    "year": "2016",
    "name": "Spring"
  },
  {
    "id": 40,
    "year": "2016",
    "name": "Winter"
  },
  {
    "id": 16,
    "year": "2015",
    "name": "Fall"
  },
  {
    "id": 38,
    "year": "2015",
    "name": "Summer"
  },
  {
    "id": 21,
    "year": "2015",
    "name": "Spring"
  },
  {
    "id": 41,
    "year": "2015",
    "name": "Winter"
  },
  {
    "id": 26,
    "year": "2014",
    "name": "Fall"
  },
  {
    "id": 6,
    "year": "2014",
    "name": "Summer"
  }
]
```
