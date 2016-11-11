# Watch
อ่านข้อมูลสำหรับดูอนิเมะที่กำหนด

type | Data
--- | ---
URL | https://www.tafasu.com/api/v1/watch
HTTP Method | GET
Parameter | limit, page, fields
Fields | hash, name, type, anime, anime.id, anime.name, anime.alias, anime.description, anime.thumbnail, anime.season, anime.season.id, anime.season.name, anime.myanimelist, anime.genre.id, anime.genre.name, anime.genre.alias, fansub, fansub.id, fansub.description, fansub.alias, fansub.facebook, fansub.cover, fansub.cover, fansub.logo, project_id, view, date, note, cover, stream, stream.name, stream.url, download, download.name,download.url
Response | JSON (Object)

## Parameter
Parameter | value
--- | ---
v | ค่า hash ของตอนที่ต้องการดู

## Fields
Fields| value
--- | ---
hash | ค่า hash ของตอนที่กำลังดู
name | ชื่อของอนิเมะตอนนั้น
type | ประเภทของตอนนั้น มีด้วยกันทั้งสิ้น 7 ประเภทได้แก่ episode, ova, oad, movie, sp ,pv ,ona
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
date | วันที่โพสอนิเมะตอนนั้น
ืnote | โน้ตจากทางแฟนซับ
cover | ภาพปกก่อนเริ่มเล่น
stream | object การสตรีมของอนิเมะเรื่องนี้
stream.name | ชื่อแหล่งไฟล์ที่ใช้ในการสตรีม
stream.url | url แหล่งไฟล์ที่ใช้ในการสตรีม
download | object สำหรับดาวน์โหลดอนิเมะตอนนี้
download.name | ชื่อแหล่งดาวน์โหลดไฟล์
download.url | url แหล่งดาวน์โหลดไฟล์
url | url สำหรับดูอนิเมะเรื่องนี้

## ตัวอย่างหน้าที่ใช้ข้อมูลดังกล่าวบนเว็บไซต์ TAFASU
![](/images/preview_watch.png)

## ตัวอย่าง json
```json
{
  "hash": "e65tVrFou2",
  "name": "04",
  "type": "episode",
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
  "project_id": 58,
  "view": "68",
  "date": "31/10",
  "note": "",
  "cover": "",
  "stream": [
    {
      "name": "koofr",
      "url": "https://app.koofr.net/content/links/15cdfdef-504d-48d9-9748-d49fb13b0e14/files/get/%5BNishikawaFS%5D%20Watashi%20ga%20Motete%20Dou%20Sunda%20-%2004%20(TBS%201280x720%20x264%20AAC).mp4?path="
    },
    {
      "name": "googledrive",
      "url": "https://drive.google.com/file/d/0B2g58_DyHypmQ3NlVFBlcmZ5Zlk/view"
    }
  ],
  "download": [
    {
      "name": "MEGA",
      "url": "https://goo.gl/UsSQfZ"
    },
    {
      "name": "Openload",
      "url": "https://goo.gl/sLNIxp"
    }
  ],
  "url": "https://www.tafasu.com/watch?v=e65tVrFou2"
}
```
