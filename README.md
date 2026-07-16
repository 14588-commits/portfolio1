# My Portfolio (เวอร์ชันเรียบง่าย)

เว็บไซต์ Portfolio ส่วนตัว 8 หน้า สร้างด้วย HTML + CSS ล้วน (ไม่มี JavaScript ซับซ้อน) พร้อม deploy บน GitHub Pages

## โครงสร้างไฟล์

```
portfolio-simple/
├── index.html          หน้าแรก
├── about.html           About Me
├── education.html       Education
├── activities.html      Activities
├── projects.html        Projects
├── awards.html          Awards & Certificates
├── skills.html          Skills
├── contact.html         Contact
├── style.css            สไตล์ทั้งหมด (ไฟล์เดียวใช้ร่วมกันทุกหน้า)
└── README.md
```

## วิธีแก้ไขเนื้อหา
เปิดไฟล์ `.html` แต่ละหน้าด้วยโปรแกรมแก้โค้ด (เช่น VS Code) แล้วแทนที่ข้อความในวงเล็บเหลี่ยม `[ ]` ด้วยข้อมูลจริงของคุณ

## วิธีแก้เมนู
เมนูด้านบน (`<nav class="navbar">`) เขียนซ้ำอยู่ในทุกไฟล์ — ถ้าจะเพิ่ม/แก้/ลบเมนู ต้องแก้ให้ครบทั้ง 8 ไฟล์ และอย่าลืมเปลี่ยน `class="active"` ให้ตรงกับหน้าปัจจุบันของแต่ละไฟล์

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

## สิ่งที่ควรทำต่อ
- [ ] แก้ข้อความในวงเล็บเหลี่ยม `[ ]` ทุกหน้าให้เป็นข้อมูลจริง
- [ ] ใส่ลิงก์ GitHub repo ของแต่ละโปรเจกต์ในหน้า `projects.html`
- [ ] ใส่อีเมล/โซเชียลจริงในหน้า `contact.html`
- [ ] ทดสอบเว็บบนมือถือ
