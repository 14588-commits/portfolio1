# My Portfolio

เว็บไซต์ Portfolio ส่วนตัว 8 หน้า สร้างด้วย HTML / CSS / JavaScript ล้วน (ไม่ต้องใช้ framework) พร้อม deploy บน GitHub Pages

## โครงสร้างไฟล์

```
portfolio/
├── index.html          หน้าแรก
├── about.html           เกี่ยวกับฉัน
├── education.html       ประวัติการศึกษา
├── activities.html      กิจกรรม
├── projects.html        ผลงาน
├── awards.html          รางวัลและใบประกาศ
├── skills.html          ทักษะ
├── contact.html         ติดต่อ
├── README.md
└── assets/
    ├── css/style.css     สไตล์ทั้งหมด (แก้สีธีมได้ที่ :root)
    ├── js/main.js        เมนูนำทาง (แก้ชื่อ/ลำดับเมนูได้ที่ตัวแปร PAGES)
    └── img/              ใส่รูปภาพของคุณที่นี่
```

## วิธีแก้ไขเนื้อหา
เปิดไฟล์ `.html` แต่ละหน้าด้วยโปรแกรมแก้โค้ด (เช่น VS Code) แล้วแทนที่ข้อความในวงเล็บเหลี่ยม `[ ]` ด้วยข้อมูลจริงของคุณ เช่น `[ชื่อโปรเจกต์ที่ 1]`

## วิธีเพิ่ม/แก้เมนู
เมนูด้านซ้าย (binder tabs) ถูกสร้างจากไฟล์เดียวคือ `assets/js/main.js` — แก้ที่ตัวแปร `PAGES` เพียงที่เดียว ทุกหน้าจะอัปเดตอัตโนมัติ

## วิธี Deploy ด้วย GitHub Pages

1. สร้าง repository ใหม่บน GitHub (public) เช่น ชื่อ `portfolio`
2. อัปโหลดไฟล์ทั้งหมดในโฟลเดอร์นี้ขึ้น repo นั้น:
   ```bash
   git init
   git add .
   git commit -m "first commit"
   git branch -M main
   git remote add origin https://github.com/<username>/<repo>.git
   git push -u origin main
   ```
3. ไปที่ repo → **Settings** → **Pages**
4. หัวข้อ **Build and deployment** → Source เลือก **Deploy from a branch**
5. เลือก branch **main** และ folder **/ (root)** แล้วกด **Save**
6. รอสักครู่ เว็บไซต์จะขึ้นที่ `https://<username>.github.io/<repo>/`

> เคล็ดลับ: ถ้าตั้งชื่อ repo เป็น `<username>.github.io` เว็บจะ deploy อัตโนมัติที่ root domain โดยไม่ต้องตั้งค่า Pages เพิ่ม

## สิ่งที่ควรทำต่อ
- [ ] ใส่รูปโปรไฟล์และรูปผลงานในโฟลเดอร์ `assets/img/`
- [ ] แก้ข้อความในวงเล็บเหลี่ยม `[ ]` ทุกหน้าให้เป็นข้อมูลจริง
- [ ] ใส่ลิงก์ GitHub repo ของแต่ละโปรเจกต์ในหน้า `projects.html`
- [ ] ทดสอบเว็บบนมือถือ (ปุ่ม MENU จะปรากฏเมื่อจอแคบกว่า 760px)
