# Anime
ใช้สำหรับอ่านรายการอนิเมะทั้งหมด และค้นหาอนิเมะ อาจประยุกต์ใช้เพื่อค้นหาอนิเมะที่มีอยู่บนเว็บ TAFASU

Type | Data
--- | --- 
URL | https://tafasu.com/api/v1/anime
HTTP Method | GET 
Parameter | limit, page, fields, name, id, type, genre, fansub, type, season, status
Fields | id, name, alias, description, thumnail, season, season.id, season.year, season.season, myanimelist, genre, genre.id, genre.name, genre.alias
Response | JSON (array)

## parameter
Parameter | value
--- | --- 
name | ชื่อเรื่องขออนิเมะนั้น สามารถใช้ wildcard (%) เพื่อแทนข้อมูลส่วนต่างๆ เช่น wata% คือชื่อเรื่องขึ้นด้วยคำว่า wata หรือ %moe คือชื่อเรื่องลงท้ายด้วย moe
id | ไอดีของอนิเมะที่จะนำมาแสดง การดึงข้อมูลของอนิเมะไอดีนั้นๆออกมา หากใช้ id ระบบจะดึงข้อมูลโดยไม่สนใจพารามิเตอร์อื่น
type | ประเภทของไฟล์อนิเมะ ได้แก่ episode, ova, oad, movie, sp, pv, ona สามารถใช้ลูกน้ำ (,) เพื่อแบ่งประเภทได้ เช่น ?type=ova,movie คือแสดงอนิเมะที่มีไฟล์ ova หรือ movie
genre | แสดงประเภทของอนิเมะ โดยจะกรอกเป็น name หรือ alias ของประเภทก็ได้ สามารถใช้ลูกน้ำเพื่อแบ่งประเภทได้
fansub | ค้นหาอนิเมะที่ทำโดยชื่อแฟนซับที่กำหนด สามารถใช้ wildcard (%) ได้ แต่ไม่สามารถใช้ลูกน้ำได้
season | ใช้บอกซีซัน ที่จะค้นหา โดยพิมพ์ชื่อซีซันติดกับปีนั้น สามารถใช้ลูกน้ำ (,) เพื่อแบ่งประเภทได้ เช่น ?season=fall2016,summer2015 จะแสดงอนิเมะที่อยู่ในในซีซั่น fall2016 หรือ summer2015
status | คือสถานะของโปรเจคที่อยู่ในอนิเมะเรื่องนั้นๆ มี 4 สถานะด้วยกันได้แก่ ongoing, complete, onhold, dropped สามมารถใช้ลูกน้ำ (,) แบ่งประเภทได้


## Fields
Fields| value
--- | --- 
id | ไอดีอนิเมะ
name | ชื่อเรื่องอนิเมะ
alias | ชื่ออนิเมะเมื่อใช้บน url ตัวอย่างเช่น www.tafasu.com/anime/amanchu
description | รายละเอียดและเรื่องย่อของอนิเมะนั้น
thumnail | รูปของอนิเมะเรื่องนั้น
season | object season ของอนิเมะเรื่องนั้น
season.id | ไอดีของซีซั่นที่อนิเมะเรื่องนี้อยู่
season.year | ปี ค.ศ. ของอนิเมะ
season.season | ซีซั่นของอนิเมะ มี 4 ซีซั่นได้แก้ Spring, Summer, Fall, Winter
myanimelist | ลิ้งค์ของ www.myanimelist.com
genre | object genre ของอนิเมะเรื่องนี้
genre.id | ไอดีของ genre อนิเมะเรื่องนี้
genre.name | ชื่อ genre ของอนิเมะเรื่องนี้
genre.alias | alias ของ genre ที่ใช้บน url เช่น www.tafasu.com/genre/action

## ตัวอย่างที่ใช้ข้อมูลส่วนนี้บนเว็บไซต์ TAFASU
![](/images/preview_anime.png)

## ตัวอย่าง json
```json
[
  {
    "id": 69,
    "name": "3X3 EYES ",
    "alias": "3x3eyes7",
    "description": "สาวน้อย \"ไป๋\" ทายาทของเผ่าสามตาผู้มีอายุกว่า 300 ปีและ \"ยาคุโมะ ฟูจิอิ\" เด็กหนุ่มธรรมดาที่ถูกไป๋ทำให้เป็นอมตะเพื่อช่วยชีวิตเขาเอาไว้ โดยทั้งคู่ได้ออกเดินทางผจญภัยและต้องต่อสู้กับปีศาจมากมายเพื่อค้นหาวิธีที่จะกลับเป็นมนุษย์ธรรมดาร่วมกัน อิงเนื้อหาต่างๆมาจากตำนานความเชื่อของฮินดูผสมกับจีนเป็นหลัก",
    "thumbnail": "1477451613.jpg",
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
    "id": 4,
    "name": "3月のライオン(Sangatsu no lion)",
    "alias": "sangatsunolion",
    "description": "คิริยามะ เรย์ เด็กหนุ่มวัย 17 ปี ที่เพิ่งย้ายมาอยู่ตัวคนเดียว มีรายได้จากการเป็นนักเล่นโชกิมืออาชีพ แต่ถึงเขาจะมีอิสระ ปัญหาต่างๆก็คอยมารบกวนชีวิตของเขา ความสัมพันธ์ระหว่างเขากับครอบครัวบุญธรรมก็เริ่มจะสั่นคลอน และเขาก็ยังมีปัญหากับการคบเพื่อนที่โรงเรียนอีกด้วย\r\nในขณะเดียวกัน อาชีพนักเล่นโชกิมืออาชีพของเขาก็เริ่มที่จะตกต่ำ เขาจึงต้องแบกรับความคาดหวังอันยิ่งใหญ่ เพราะทั้งการแพ้และชนะมีผลต่อหน้าที่การงานของเขาทั้งสิ้น\r\nคนรู้จักของเรย์ก็คือ พี่น้องคาวาโมโตะ อาคาริ ฮินาตะ และ โมโมะ ซึ่งต่างจากเรย์ พวกเธออยู่อย่างมีความสุขในบ้านธรรมดาๆ ที่พร้อมจะต้อนรับเรย์เหมือนกับพี่น้องของพวกเธอ เรย์นั้นได้รับความรักความอบอุ่น ต่างจากบ้านของผู้อุปถัมภ์อย่างสิ้นเชิง\r\nอนิเมะเรื่องนี่จะกล่าวถึง ชัยชนะอันงดงาม ความผิดพลาด ความสัมพันธ์ใหม่-เก่า และการเติบโตเป็นผู้ใหญ่ ของ คิริยามะ เรย์",
    "thumbnail": "1477231251.jpg",
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
  }
]
```
