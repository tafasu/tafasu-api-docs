# Schedule day
อ่านโปรเจคที่มีกำหนดการปล่อยในวันที่กำหนด โดยแทน day ด้วย today,sunday,monday,tuesday, wednesday, thursday, friday, saturday ซึ่งใช้สำหรับหารหัสโปรเจค เพื่อนำไปหาตอนอนิเมะใน /project/:id เป็นลำดับถัดไป

Type | Data
--- | ---
URL | https://www.tafasu.com/api/v1/schedule/:day
HTTP Method | GET
Parameter | limit, page, fields
Fields | id, anime, anime.id, anime.name, anime.alias, anime.description, anime.thumbnail, anime.season, anime.season.id, anime.season.name, anime.myanimelist, anime.genre.id, anime.genre.name, anime.genre.alias, fansub, fansub.id, fansub.description, fansub.alias, fansub.facebook, fansub.cover, fansub.cover, fansub.logo
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
id | รหัสไอดีของโปรเจคที่แฟนซับทำอยู่ในเรื่องนั้น
schedule | วันที่จะปล่อยอนิเมะเรื่องนั้นๆ มี 7 วันได้แก่ sunday, monday, ... , saturday
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

## ตัวอย่างหน้าที่ใช้ข้อมูลดังกล่าวบนเว็บไซต์ TAFASU
![](/images/preview_schedule_day.png)

## ตัวอย่าง json
```json
[
  {
    "id": 50,
    "schedule": "friday",
    "anime": {
      "id": 13,
      "name": "Fune wo Amu",
      "alias": "funewoamu",
      "description": "การตีพิมพ์พจนานุกรมเล่มใหม่ นามว่า \"การข้ามทะเลครั้งยิ่งใหญ่\" กำลังดำเนินการ มิทซูยะ มาจิเมะ ที่เคยเป็นเซลล์แมนของสำนักพิมพ์ เกนบู ได้ถูก โควเฮย์ อารากิ บรรณานุกรมโคตรเทพแห่งแผนกบรรณาธิการพจนานุกรมที่กำลังจะเกษียณไปฝึกงาน โดยที่แผนกนี้เคยถูกเรียกว่า \"ไม่กินเงิน\" แต่มิทซูยะก็ใช้ความสามารถของเขากับคำศัพท์ต่างๆ ที่จะเป็นบรรณานุกรมระดับเทพให้ได้ แต่มิทซูยะนั้น มนุษยสัมพันธ์ไม่ค่อยดีนัก ซึ่งได้ทำงานกับ มาซาชิ นิชิโอกะ ที่สามารถอธิบายตัวเองได้ดีกว่า",
      "thumbnail": "https://www.tafasu.com/upload/img/1477231190.jpg",
      "season": {
        "id": "1",
        "year": "2016",
        "name": "Fall"
      },
      "myanimelist": "https://myanimelist.net/anime/32948/Fune_wo_Amu",
      "genre": [
        {
          "id": 7,
          "name": "Drama",
          "alias": "drama"
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
    ]
  },
  {
    "id": 137,
    "schedule": "friday",
    "anime": {
      "id": 5,
      "name": "Haikyuu!!: Karasuno Koukou VS Shiratorizawa Gakuen Koukou",
      "alias": "haikyuu!!",
      "description": "ทีมวอลเลย์บอลคาราสึโนะกับรอบชิงชนะเลิศหาตัวเเทนเพื่อไปเเข่งระดับประเทศ เเล้วเเมชต์สุดท้ายนี้ต้องเจอราชาจากชิราโทริซาว่า เเล้วอดีตอีกาบินไม่ได้ จะเอาชนะอินทรีย์ขาวได้หรือไม่ ติดตามกันได้เลยค่ะ",
      "thumbnail": "https://www.tafasu.com/upload/img/1478015716.jpg",
      "season": {
        "id": "1",
        "year": "2016",
        "name": "Fall"
      },
      "myanimelist": "https://myanimelist.net/anime/32935/Haikyuu__Karasuno_Koukou_VS_Shiratorizawa_Gakuen_Koukou?q=haikyuu",
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
          "id": 35,
          "name": "School",
          "alias": "school"
        },
        {
          "id": 42,
          "name": "Shounen",
          "alias": "shounen"
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
        "id": 129,
        "name": "YL_FS",
        "description": "Auto Generated by TAFASU",
        "alias": "ylfs",
        "facebook": "",
        "cover": "",
        "logo": ""
      },
      {
        "id": 136,
        "name": "ZouL Fansub",
        "description": "Beyond the Sky, We find our ZouL",
        "alias": "zoulfs",
        "facebook": "https://www.facebook.com/631298717013118",
        "cover": "http://i.imgur.com/VGj9r4O.png",
        "logo": "1476097115.png"
      }
    ]
  }
]
```
