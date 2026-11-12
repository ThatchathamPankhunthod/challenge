# POWER UP! — Creative Space Demo

ตัวอย่างหน้าเว็บ POWER UP! ที่ต่อยอดจาก Full Web Demo โดยเพิ่มองค์ประกอบ Gamification ตามหัวข้อ Creative Space ได้แก่ Challenge Card, XP, Level และ Badge

## ไฟล์ในโปรเจกต์
- `index.html` — หน้าเว็บหลัก พร้อม Dashboard, Challenge Exchange, My Portfolio และส่วน XP/Badge
- `css/style.css` — รูปแบบหน้าเว็บและ Responsive Design
- `js/app.js` — Import/Export Challenge, Validation, Complete Challenge, Portfolio และระบบ XP/Badge
- `data/challenge-*.json` — Challenge ตัวอย่าง 3 ประเภท

## วิธีเปิดใช้งาน
1. แตกไฟล์ ZIP
2. เปิดโฟลเดอร์ `POWER-UP-Creative-Space-Demo` ใน VS Code
3. ติดตั้งส่วนขยาย Live Server (ถ้ายังไม่มี)
4. คลิกขวา `index.html` แล้วเลือก **Open with Live Server**

## สิ่งที่เพิ่มใน Creative Space
- **Challenge Card:** แสดงประเภท เวลา และ XP Reward ของแต่ละภารกิจ
- **XP:** เมื่อบันทึก Reflection และ Complete Challenge สำเร็จ จะได้รับ XP ตามประเภท
  - Discover = 100 XP
  - Mix Skills = 150 XP
  - Level Up = 200 XP
  - สามารถกำหนด `xpReward` เป็นตัวเลขเพิ่มเติมใน JSON ได้ (ถ้าไม่กำหนด ระบบใช้ค่าตาม Category)
- **Level:** ทุก 300 XP จะเพิ่ม 1 Level พร้อมแถบความคืบหน้า
- **Badge:** มี 5 รางวัล ได้แก่ First Spark, Mix Master, Level Up, Challenge Trio และ Portfolio Builder
- **Persistence:** XP, Level, Badge และผลงานอ้างอิงจาก Challenge ที่ทำสำเร็จ และข้อมูลถูกเก็บใน localStorage ของ Browser

## วิธีทดลอง
1. เลื่อนลงมาที่ Challenge Exchange
2. กดรายละเอียดของ Challenge
3. กด Complete Challenge
4. กรอก Reflection และ Evidence ให้ครบ แล้วกด Save Portfolio Item
5. กลับไปดู XP, Level และ Badge ใน Dashboard
6. ทดลองทำ Challenge ประเภท Mix Skills หรือ Level Up เพื่อปลดล็อก Badge เฉพาะประเภท

## ข้อจำกัดสำคัญ
นี่คือ **Frontend Prototype** สำหรับสาธิตแนวคิด Creative Space เท่านั้น ข้อมูลยังเก็บใน `localStorage` ของ Browser เครื่องนั้น ไม่ได้เชื่อม Backend / AWS EC2 และยังไม่รองรับการซิงก์ XP หรือ Badge ข้ามอุปกรณ์
