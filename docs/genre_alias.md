# Genre Alias
ใช้สำหรับอ่านรายการอนิเมะทั้งหมด ที่อยู่ในประเภทที่กำหนด ใช้ alias หรือ id ในการระบุประเภท โดยข้อมูลที่ตอบกลับมานั้นจะเรียงชื่อเรื่องตามตัวอักษร

Type | Data
--- | ---
URL | https://www.tafasu.com/api/v1/genre/:alias
HTTP Method | GET
Parameter | limit, page, fields,
Fields | id, name, alias, description, thumbnail, season, season.id, season.year, season.season, myanimelist, genre, genre.id, genre.name, genre.alias
Response | JSON (object)

## Parameter
Parameter | value
--- | ---
limit | บอกจำนวนข้อมูลที่จะดึงมาแสดง ตั้งแต่ 0-100 (ค่าเริ่มต้น 10)
page | หน้าข้อมูลปัจจุบัน
fields | ฟิลล์ข้อมูลที่จะนำมาแสดง แบ่งด้วยลูกน้ำ (,)


## Fields
Fields| value
--- | ---
id | ไอดีอนิเมะ
name | ชื่อเรื่องอนิเมะ
alias | ชื่ออนิเมะเมื่อใช้บน url ตัวอย่างเช่น www.tafasu.com/anime/amanchu
description | รายละเอียดและเรื่องย่อของอนิเมะนั้น
thumbnail | รูปของอนิเมะเรื่องนั้น
season | object season ของอนิเมะเรื่องนั้น
season.id | ไอดีของซีซั่นที่อนิเมะเรื่องนี้อยู่
season.year | ปี ค.ศ. ของอนิเมะ
season.name | ซีซั่นของอนิเมะ มี 4 ซีซั่นได้แก้ Spring, Summer, Fall, Winter
myanimelist | ลิ้งค์ของ www.myanimelist.com
genre | object genre ของอนิเมะเรื่องนี้
genre.id | ไอดีของ genre อนิเมะเรื่องนี้
genre.name | ชื่อ genre ของอนิเมะเรื่องนี้
genre.alias | alias ของ genre ที่ใช้บน url เช่น www.tafasu.com/genre/action

## ตัวอย่างหน้าที่ใช้ข้อมูลดังกล่าวบนเว็บไซต์ TAFASU
![](/images/preview_genre_alias.png)

## ตัวอย่าง json
```json
[
  {
    "id": 69,
    "name": "3X3 EYES ",
    "alias": "3x3eyes7",
    "description": "สาวน้อย \"ไป๋\" ทายาทของเผ่าสามตาผู้มีอายุกว่า 300 ปีและ \"ยาคุโมะ ฟูจิอิ\" เด็กหนุ่มธรรมดาที่ถูกไป๋ทำให้เป็นอมตะเพื่อช่วยชีวิตเขาเอาไว้ โดยทั้งคู่ได้ออกเดินทางผจญภัยและต้องต่อสู้กับปีศาจมากมายเพื่อค้นหาวิธีที่จะกลับเป็นมนุษย์ธรรมดาร่วมกัน อิงเนื้อหาต่างๆมาจากตำนานความเชื่อของฮินดูผสมกับจีนเป็นหลัก",
    "thumbnail": "https://www.tafasu.com/upload/img/1477451613.jpg",
    "season": {
      "id": 27,
      "year": "1991",
      "name": "Summer"
    },
    "myanimelist": "",
    "genre": [
      {
        "id": 1,
        "name": "Action",
        "alias": "action"
      },
      {
        "id": 2,
        "name": "Adventure",
        "alias": "adventure"
      },
      {
        "id": 6,
        "name": "Demons",
        "alias": "demons"
      },
      {
        "id": 20,
        "name": "Magic",
        "alias": "magic"
      },
      {
        "id": 26,
        "name": "Mystery",
        "alias": "mystery"
      }
    ]
  },
  {
    "id": 37,
    "name": "Ai to Ken no Camelot Mangaka Marina Time Slip",
    "alias": "Camelotova",
    "description": "มารินะและหนุ่มหล่อร่วมฉลองวันเกิดเพื่อนได้หลุดเข้าไปในยุคกลางอังกฤษและให้การช่วยเหลืออาเธอร์ เพนดรากอนในการปกครองคาเมล็อต",
    "thumbnail": "https://www.tafasu.com/upload/img/1477316400.jpg",
    "season": {
      "id": 4,
      "year": "1990",
      "name": "Summer"
    },
    "myanimelist": "",
    "genre": [
      {
        "id": 1,
        "name": "Action",
        "alias": "action"
      },
      {
        "id": 2,
        "name": "Adventure",
        "alias": "adventure"
      },
      {
        "id": 15,
        "name": "Historical",
        "alias": "historical"
      },
      {
        "id": 29,
        "name": "OVA",
        "alias": "ova"
      }
    ]
  }
]```
