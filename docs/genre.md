# Genre
อ่านประเภทอนิเมะทั้งหมด

Type | Data
--- | ---
URL | https://www.tafasu.com/api/v1/genre
HTTP Method | GET
Parameter | limit, page, fields, id, name, alias
Fields |id, name, alias
Response | JSON (array)

## Parameter
Parameter | value
--- | ---
limit | บอกจำนวนข้อมูลที่จะดึงมาแสดง ตั้งแต่ 0-100 (ค่าเริ่มต้น 10)
page | หน้าข้อมูลปัจจุบัน
fields | ฟิลล์ข้อมูลที่จะนำมาแสดง แบ่งด้วยลูกน้ำ (,)
id | แสดงข้อมูลประเภทของไอดีที่กำหนด
name | แสดงข้อมูลประเภทของชื่อประเภทที่กำหนด โดยสามารถใช้ wildcard (%) ได้
alias | แสดงข้อมูลประเภทของ alias ประเภทที่กำหนด โดยสามารถใช้ wildcard (%) ได้

## Fields
Fields| value
--- | ---
id | ไอดีของประเภทนี้
name | ชื่อของประเภทนี้
alias | alias ของประเภท ที่ใช้บน url เช่น www.tafasu.com/genre/action


## ตัวอย่างหน้าที่ใช้ข้อมูลดังกล่าวบนเว็บไซต์ TAFASU
![](/images/preview_genre.png)

## ตัวอย่าง json
```json
[
  {
    "id": 1,
    "genre": "Action",
    "alias": "action"
  },
  {
    "id": 2,
    "genre": "Adventure",
    "alias": "adventure"
  },
  {
    "id": 3,
    "genre": "Cars",
    "alias": "cars"
  },
  {
    "id": 4,
    "genre": "Comedy",
    "alias": "comedy"
  },
  {
    "id": 5,
    "genre": "Cyberpunk",
    "alias": "cyberpunk"
  },
  {
    "id": 6,
    "genre": "Demons",
    "alias": "demons"
  },
  {
    "id": 7,
    "genre": "Drama",
    "alias": "drama"
  },
  {
    "id": 8,
    "genre": "Ecchi",
    "alias": "ecchi"
  },
  {
    "id": 9,
    "genre": "Fantasy",
    "alias": "fantasy"
  },
  {
    "id": 10,
    "genre": "Flash Animation",
    "alias": "flash-animation"
  }
]
```
