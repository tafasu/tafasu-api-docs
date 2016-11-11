# Fansub Recent work
อ่านอนิเมะตอนล่าสุดที่แฟนซับนี้โพส

Type | Data
--- | ---
URL | https://www.tafasu.com/api/v1/fabsub/:alias/recent
HTTP Method | GET
Parameter | limit, page, fields
Fields | hash, name, type, date, anime, anime.id, anime.name, anime.alias, anime.description, anime.thumbnail, anime.season, anime.season.id, anime.season.name, anime.myanimelist, anime.genre.id, anime.genre.name, anime.genre.alias, fansub, fansub.id, fansub.description, fansub.alias, fansub.facebook, fansub.cover, fansub.cover, fansub.logo, url, project_id, status
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
hash | ค่า hash สำหรับหาข้อมูลอนิเมะเรื่องนั้นจาก /watch
name | ชื่อของอนิเมะตอนนั้น
type | ประเภทของตอนนั้น มีด้วยกันทั้งสิ้น 7 ประเภทได้แก่ episode, ova, oad, movie, sp ,pv ,ona
date | วันที่โพสอนิเมะตอนนั้น
anime | object anime ของโปรเจคนี้
anime.id | ไอดีอนิเมะ
anime.name | ชื่อเรื่องอนิเมะ
anime.alias | ชื่ออนิเมะเมื่อใช้บน url ตัวอย่างเช่น www.tafasu.com/anime/amanchu
anime.description | รายละเอียดและเรื่องย่อของอนิเมะนั้น
anime.thumbnail | รูปของอนิเมะเรื่องนั้น
anime.season | object season ของอนิเมะเรื่องนั้น
anime.season.id | ไอดีของซีซั่นที่อนิเมะเรื่องนี้อยู่
anime.season.year | ปี ค.ศ. ของอนิเมะ
anime.season.name | ซีซั่นของอนิเมะ มี 4 ซีซั่นได้แก้ Spring, Summer, Fall, Winter
anime.myanimelist | ลิ้งค์ของ www.myanimelist.com
anime.genre | object genre ของอนิเมะเรื่องนี้
anime.genre.id | ไอดีของ genre อนิเมะเรื่องนี้
anime.genre.name | ชื่อ genre ของอนิเมะเรื่องนี้
anime.genre.alias | alias ของ genre ที่ใช้บน url เช่น www.tafasu.com/genre/action
fansub | อาเรย์ของรายชื่อแฟนซับที่ทำโปรเจคนั้นอยู่
fansub.id | รหัสไอดีของแฟนซับนั้น
fansub.description | คำโปรยของแฟนซับนั้น
fansub.alias | ชื่อแฟนซับสำหรับใช้ใน url ตัวอย่างเช่น www.tafasu.com/fansub/nishikawafs
fansub.facebook | url เพจเฟสบุ๊คของแฟนซับนั้นๆ
fansub.cover | ภาพพื้นหลังของแฟนซับนั้นๆ
fansub.logo | ภาพโลโก้ของแฟนซับนั้นๆ
ีurl | url สำหรับดูอนิเมะตอนนั้นบน TAFASU
project_id | โปรเจคไอดีตอนนั้น สำหรับค้นหาบน /project/:id
status | สถานะของโปรเจคนั้นมีด้วยกัน 5 ประเภท ได้แก่ Ongoing, Complete, OnHold, Dropped, Licensed

## ตัวอย่างหน้าที่ใช้ข้อมูลดังกล่าวบนเว็บไซต์ TAFASU
![](/images/preview_fansub_recent.png)

## ตัวอย่าง json
```json
[
  {
    "hash": "e65tVrFou2",
    "episode": "04",
    "type": "episode",
    "date": "31/10",
    "anime": {
      "id": 33,
      "name": "Watashi ga Motete Dousunda",
      "alias": "watashigamotetedousunda",
      "description": "เซรินูมะ คาเอะ สาวฟุโจชิที่อ้วนท้วม เมื่อตัวละครโปรดของเธอตายทำให้เครียดและเศร้าอย่างมาก จนน้ำหนักลดลงอย่างรวดเร็ว หลังกลับมาชั้นเรียน เธอกลายเป็นสาวที่มีเสน่ห์ จนมีหนุ่มหลายคนตามจีบ แต่ความเป็นสาว Y ของเธอยังคงเหมือนเดิม",
      "thumbnail": "https://www.tafasu.com/upload/img/1477222364.jpg",
      "season": {
        "id": "1",
        "year": "2016",
        "name": "Fall"
      },
      "myanimelist": "https://myanimelist.net/anime/32899/Watashi_ga_Motete_Dousunda",
      "genre": [
        {
          "id": 4,
          "name": "Comedy",
          "alias": "comedy"
        },
        {
          "id": 14,
          "name": "Harem",
          "alias": "harem"
        },
        {
          "id": 33,
          "name": "Romance",
          "alias": "romance"
        },
        {
          "id": 35,
          "name": "School",
          "alias": "school"
        },
        {
          "id": 40,
          "name": "Shoujo",
          "alias": "shoujo"
        }
      ]
    },
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
    "url": "https://www.tafasu.com/watch?v=e65tVrFou2",
    "project_id": 58,
    "status": "Ongoing"
  },
  {
    "hash": "FZRuIQ8Syo",
    "episode": "12",
    "type": "episode",
    "date": "31/10",
    "anime": {
      "id": 160,
      "name": "Owari no Seraph: Nagoya Kessen-hen",
      "alias": "seraphs2",
      "description": "โลกที่มีไวรัสปริศนาที่ทำให้มนุษย์ที่อายุเกิน 13 ติดเชื้อและล้มตายกัน เหลือเพียงเด็กและพวกแวมไพร์ได้เข้ามายึดครองโลก ทำให้มนุษยชาติต้องกลายเป็นทาสบริวารและแหล่งอาหารของพวกมัน เรื่องราวของ เฮียคุยะ ยูอิจิโร่ เด็กหนุ่มที่ถูกส่งมาที่สถานเด็กกำพร้าเพื่อเป็นแหล่งอาหารให้พวกแวมไพร์ เขาฝันที่จะกวาดล้างพวกแวมไพร์ทั้งหมดบนโลกนี้ และได้ลุกขึ้นสู้ต่อต้านพวกแวมไพร์",
      "thumbnail": "https://www.tafasu.com/upload/img/1477919859.jpg",
      "season": {
        "id": "16",
        "year": "2015",
        "name": "Fall"
      },
      "myanimelist": "https://myanimelist.net/anime/28927/Owari_no_Seraph__Nagoya_Kessen-hen",
      "genre": [
        {
          "id": 1,
          "name": "Action",
          "alias": "action"
        },
        {
          "id": 7,
          "name": "Drama",
          "alias": "drama"
        },
        {
          "id": 42,
          "name": "Shounen",
          "alias": "shounen"
        },
        {
          "id": 48,
          "name": "Supernatural",
          "alias": "supernatural"
        },
        {
          "id": 51,
          "name": "Vampire",
          "alias": "vampire"
        }
      ]
    },
    "fansub": [
      {
        "id": 57,
        "name": "ItaiIku-FS",
        "description": "Auto Generated by TAFASU",
        "alias": "itaikufs",
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
    ],
    "url": "https://www.tafasu.com/watch?v=FZRuIQ8Syo",
    "project_id": 257,
    "status": "Complete"
  }
]
```
