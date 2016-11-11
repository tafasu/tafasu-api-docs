# Project id
อ่านโปรเจค โดยข้อมูลที่กำหนด

Type | Data
--- | ---
URL | https://www.tafasu.com/api/v1/project
HTTP Method | GET
Parameter | fields,
Fields | id, anime, anime.id, anime.name, anime.alias, anime.description, anime.thumbnail, anime.season, anime.season.id, anime.season.name, anime.myanimelist, anime.genre.id, anime.genre.name, anime.genre.alias, fansub, fansub.id, fansub.description, fansub.alias, fansub.facebook, fansub.cover, fansub.cover, fansub.logo1
Response | JSON (Object)

## Parameter
Parameter | value
--- | ---
fields | ฟิลล์ข้อมูลที่จะนำมาแสดง แบ่งด้วยลูกน้ำ (,)


## Fields
Fields| value
--- | ---
id | รหัสไอดีของโปรเจคที่แฟนซับทำอยู่ในเรื่องนั้น
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
status | สถานะของโปรเจคนั้น มี 5 สถานนะได้แก่ (Ongoing,OnHold,Complete,Dropped,Licensed)

## ตัวอย่างหน้าที่ใช้ข้อมูลดังกล่าวบนเว็บไซต์ TAFASU

**ไม่มีภาพของส่วนนี้ใน TAFASU**

## ตัวอย่าง json
```json
{
  "id": 49,
  "anime": {
    "id": 4,
    "name": "3月のライオン(Sangatsu no lion)",
    "alias": "sangatsunolion",
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
  "fansub": [
    {
      "id": 113,
      "name": "Shiniji-FS",
      "description": "แฟนซับของเหล่าเด็กน้อย ม.ปลายสี่หน่อ ที่อยู่บ้างไม่อยู่บ้าง ตามภาระงานที่มี ผลงานของพวกเขา จะยอดเยี่ยม หรือ ยอดแย่กันแน่ ติดตามได้ที่ Shiniji-FS เลยจ้า（＞ｗ＜）",
      "alias": "shinijifansub",
      "facebook": "",
      "cover": "http://i.imgur.com/a0Z7IK2.jpg",
      "logo": "1477404410.jpg"
    }
  ],
  "status": "Ongoing"
}
```
