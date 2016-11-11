# Anime Data
อ่านข้อมูลของอนิเมะเรื่องที่กำหนด โดยใช้ alias หรือ id ตัวอย่างเช่น  https://www.tafasu.com/api/v1/anime/watashigamotetedousunda หรือ https://www.tafasu.com/api/v1/anime/33 จะได้ข้อมูลของอนิเมะเรื่อง Watashi ga Motete Dousunda กลับมา

Type | Data
--- | ---
URL | https://www.tafasu.com/api/v1/anime/:alias
HTTP Method | GET
Parameter | fields
Fields | id, name, alias, description, thumbnail, season, season.id, season.year, season.season, myanimelist, genre, genre.id, genre.name, genre.alias
Response | JSON (object)

## Parameter
Parameter | value
--- | ---
fields | ฟิลล์ข้อมูลที่จะนำมาแสดง แบ่งด้วยลูกน้ำ (,)


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

## ตัวอย่างหน้าที่ใช้ข้อมูลดังกล่าวบนเว็บไซต์ TAFASU
![](/images/preview-anime-alias.png)

## ตัวอย่าง json
```json
{
  "id": 33,
  "name": "Watashi ga Motete Dousunda",
  "alias": "watashigamotetedousunda",
  "description": "เซรินูมะ คาเอะ สาวฟุโจชิที่อ้วนท้วม เมื่อตัวละครโปรดของเธอตายทำให้เครียดและเศร้าอย่างมาก จนน้ำหนักลดลงอย่างรวดเร็ว หลังกลับมาชั้นเรียน เธอกลายเป็นสาวที่มีเสน่ห์ จนมีหนุ่มหลายคนตามจีบ แต่ความเป็นสาว Y ของเธอยังคงเหมือนเดิม",
  "thumbnail": "1477222364.jpg",
  "season": {
    "id": 1,
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
}
```
