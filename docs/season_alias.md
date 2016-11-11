# Season Anime
ใช้สำหรับอ่านอนิเมะทั้งหมดที่อยู่ในซีซั่นนั้น โดยจะใช้ ไอดี เช่น /season/1 หรือใช้ชื่อ season เช่น /season/fall2016 ก็ได้

Type | Data
--- | ---
URL | https://www.tafasu.com/api/v1/season/:alias
HTTP Method | GET
Parameter | limit, page, fields
Fields | id, name, alias, description, thumbnail, season, season.id, season.year, season.season, myanimelist, genre, genre.id, genre.name, genre.alias
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
![](/images/preview_season_alias.png)

## ตัวอย่าง json
```json
[
  {
    "id": 4,
    "name": "3月のライオン(Sangatsu no lion)",
    "alias": "sangatsunolion",
    "description": "คิริยามะ เรย์ เด็กหนุ่มวัย 17 ปี ที่เพิ่งย้ายมาอยู่ตัวคนเดียว มีรายได้จากการเป็นนักเล่นโชกิมืออาชีพ แต่ถึงเขาจะมีอิสระ ปัญหาต่างๆก็คอยมารบกวนชีวิตของเขา ความสัมพันธ์ระหว่างเขากับครอบครัวบุญธรรมก็เริ่มจะสั่นคลอน และเขาก็ยังมีปัญหากับการคบเพื่อนที่โรงเรียนอีกด้วย\r\nในขณะเดียวกัน อาชีพนักเล่นโชกิมืออาชีพของเขาก็เริ่มที่จะตกต่ำ เขาจึงต้องแบกรับความคาดหวังอันยิ่งใหญ่ เพราะทั้งการแพ้และชนะมีผลต่อหน้าที่การงานของเขาทั้งสิ้น\r\nคนรู้จักของเรย์ก็คือ พี่น้องคาวาโมโตะ อาคาริ ฮินาตะ และ โมโมะ ซึ่งต่างจากเรย์ พวกเธออยู่อย่างมีความสุขในบ้านธรรมดาๆ ที่พร้อมจะต้อนรับเรย์เหมือนกับพี่น้องของพวกเธอ เรย์นั้นได้รับความรักความอบอุ่น ต่างจากบ้านของผู้อุปถัมภ์อย่างสิ้นเชิง\r\nอนิเมะเรื่องนี่จะกล่าวถึง ชัยชนะอันงดงาม ความผิดพลาด ความสัมพันธ์ใหม่-เก่า และการเติบโตเป็นผู้ใหญ่ ของ คิริยามะ เรย์",
    "thumbnail": "https://www.tafasu.com/upload/img/1477231251.jpg",
    "season": {
      "id": 1,
      "year": "2016",
      "name": "Fall"
    },
    "myanimelist": "https://myanimelist.net/anime/31646/3-gatsu_no_Lion?q=3%20gatsu",
    "genre": [
      {
        "id": 4,
        "name": "Comedy",
        "alias": "comedy"
      },
      {
        "id": 7,
        "name": "Drama",
        "alias": "drama"
      },
      {
        "id": 11,
        "name": "Game",
        "alias": "game"
      },
      {
        "id": 37,
        "name": "Seinen",
        "alias": "seinen"
      },
      {
        "id": 44,
        "name": "Slice of Life",
        "alias": "slice-of-lice"
      },
      {
        "id": 47,
        "name": "Sports",
        "alias": "sports"
      }
    ]
  },
  {
    "id": 239,
    "name": "aaa",
    "alias": "aaa",
    "description": "aaaa",
    "thumbnail": "",
    "season": {
      "id": 1,
      "year": "2016",
      "name": "Fall"
    },
    "myanimelist": "https://myanimelist.net/anime/31988",
    "genre": []
  }
]
```
