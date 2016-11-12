#New Release Anime
ใช้สำหรับอ่านอนิเมะตอนที่เพิ่งถูกเพิ่มเข้ามา โดยข้อมูลที่ตอบกลับมานั้นจะเรียงตามเวลา

Type | Data
--- | ---
URL | https://www.tafasu.com/api/v1/anime/recent
HTTP Method | GET
Parameter | limit, page, fields
Fields | hash, name, type, anime.id, anime.name, anime.alias, anime.description, anime.thumbnail, anime.season, anime.season.id, anime.season.year, anime.season.name, anime.myanimelist,anime.genre, anime.genre.id, anime.genre.name, anime.genre.alias, fansub, fansub.id, fansub.name, fansub.description, fansub.alias, fansub.facebook, fansub.cover, fansub.logo, project_id, view, date, url
Response | JSON (array)

## Parameter
Parameter | Value
--- | ---
limit | บอกจำนวนข้อมูลที่จะดึงมาแสดง ตั้งแต่ 0-100 (ค่าเริ่มต้น 10)
page | หน้าข้อมูลปัจจุบัน
fields | ฟิลล์ข้อมูลที่จะนำมาแสดง แบ่งด้วยลูกน้ำ (,)


## Fields
Fields| value
--- | ---
hash | ค่า hash ของอนิเมะตอนนั้นสำหรับใช้ดึงข้อมูลผ่าน /watch/:hash
name | ชื่อตอนที่ถูกเพิ่มเข้ามา
type | ประเภทของตอนที่ถูกเพิ่มเข้ามา มีด้วยกันทั้งสิ้น 7 ประเภทคือ (episode,ova,oad,movie,sp,pv,ona)
anime.id | ไอดีอนิเมะ
anime.name | ชื่อเรื่องอนิเมะ
anime.alias | ชื่ออนิเมะเมื่อใช้บน url ตัวอย่างเช่น www.tafasu.com/anime/amanchu
anime.description | รายละเอียดและเรื่องย่อของอนิเมะนั้น
anime.thumbnail | รูปของอนิเมะเรื่องนั้น
anime.season | object season ของอนิเมะเรื่องนั้น
anime.season.id | ไอดีของซีซั่นที่อนิเมะเรื่องนี้อยู่
anime.season.year | ปี ค.ศ. ของอนิเมะ
anime.season.season | ซีซั่นของอนิเมะ มี 4 ซีซั่นได้แก้ Spring, Summer, Fall, Winter
anime.myanimelist | ลิ้งค์ของ www.myanimelist.com
anime.genre | object genre ของอนิเมะเรื่องนี้
anime.genre.id | ไอดีของ genre อนิเมะเรื่องนี้
anime.genre.name | ชื่อ genre ของอนิเมะเรื่องนี้
anime.genre.alias | alias ของ genre ที่ใช้บน url เช่น www.tafasu.com/genre/action
project_id | ไอดีของโปรเจคที่อนิเมะตอนนั้นอยู่ใช้ดึงข้อมูลผ่าน /project/:id
view | จำนวนผู้ชมอนิเมะตอนนั้น
date | วันเวลาที่อัปโหลดอนิเมะตอนนั้น ตอบในรูป วัน/เดือน ตัวอย่างเช่น 14/11
url | url สำหรับดูอนิเมะตอนนั้น ตัวอย่างเช่น https://www.tafasu.com/watch?v=2oTzSAtn3X

## ตัวอย่างหน้าที่ใช้ข้อมูลดังกล่าวบนเว็บไซต์ TAFASU
![](/images/preview_anime_recent.png)

## ตัวอย่าง json
```json
[
  {
    "hash": "2oTzSAtn3X",
    "name": "02",
    "type": "episode",
    "anime": {
      "id": 241,
      "name": "C³",
      "alias": "c3",
      "description": "From the light novel series written by Minase Hazuki, comes a story of love, action, and comedy. Yachi Haruaki is a high school boy who is naturally resistant to curses. After his father sends him a mysterious black cube, Haruaki awakes to find a nude girl named Fear standing in his kitchen. She’s the human form of the cursed black cube – and an instrument of torture! Utilizing her special abilities, Fear fights alongside Haruaki to defeat other cursed instruments and their owners.\r\n",
      "thumbnail": "",
      "season": {
        "id": "64",
        "year": "2011",
        "name": "Fall"
      },
      "myanimelist": "https://myanimelist.net/anime/10578",
      "genre": [
        {
          "id": 1,
          "name": "Action",
          "alias": "action"
        },
        {
          "id": 4,
          "name": "Comedy",
          "alias": "comedy"
        },
        {
          "id": 8,
          "name": "Ecchi",
          "alias": "ecchi"
        },
        {
          "id": 35,
          "name": "School",
          "alias": "school"
        },
        {
          "id": 48,
          "name": "Supernatural",
          "alias": "supernatural"
        }
      ]
    },
    "fansub": [
      {
        "id": 248,
        "name": "Pure app",
        "description": "",
        "alias": "pureapp",
        "facebook": "",
        "cover": "",
        "logo": ""
      }
    ],
    "project_id": 362,
    "view": "5",
    "date": "06/11",
    "url": "https://www.tafasu.com/watch?v=2oTzSAtn3X"
  },
  {
    "id": 1662,
    "name": "01",
    "type": "episode",
    "anime": {
      "id": 241,
      "name": "C³",
      "alias": "c3",
      "description": "From the light novel series written by Minase Hazuki, comes a story of love, action, and comedy. Yachi Haruaki is a high school boy who is naturally resistant to curses. After his father sends him a mysterious black cube, Haruaki awakes to find a nude girl named Fear standing in his kitchen. She’s the human form of the cursed black cube – and an instrument of torture! Utilizing her special abilities, Fear fights alongside Haruaki to defeat other cursed instruments and their owners.\r\n",
      "thumbnail": "",
      "season": {
        "id": "64",
        "year": "2011",
        "name": "Fall"
      },
      "myanimelist": "https://myanimelist.net/anime/10578",
      "genre": [
        {
          "id": 1,
          "name": "Action",
          "alias": "action"
        },
        {
          "id": 4,
          "name": "Comedy",
          "alias": "comedy"
        },
        {
          "id": 8,
          "name": "Ecchi",
          "alias": "ecchi"
        },
        {
          "id": 35,
          "name": "School",
          "alias": "school"
        },
        {
          "id": 48,
          "name": "Supernatural",
          "alias": "supernatural"
        }
      ]
    },
    "fansub": [
      {
        "id": 248,
        "name": "Pure app",
        "description": "",
        "alias": "pureapp",
        "facebook": "",
        "cover": "",
        "logo": ""
      },
      {
        "id": 0,
        "name": "WEZ translation",
        "description": "",
        "alias": "",
        "facebook": "",
        "cover": "",
        "logo": ""
      }
    ],
    "hash": "iC34f6G7vH",
    "project_id": 361,
    "view": "4",
    "date": "06/11",
    "url": "https://www.tafasu.com/watch?v=iC34f6G7vH"
  }
]
```
