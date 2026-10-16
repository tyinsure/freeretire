# TYINSURE Flexi Retire — GitHub Pages

เว็บแอปเวอร์ชันล่าสุดสำหรับคำนวณทั้ง 6 แผน จากทุนประกันหรือเบี้ยรายปี
พร้อมกราฟ ตารางรายปี ดาวน์โหลด Excel และ PDF

## วิธีนำขึ้น GitHub Pages

1. แตกไฟล์ ZIP นี้ก่อน (ไม่ต้องอัปโหลดไฟล์ ZIP เข้า repository)
2. สร้าง repository ใหม่บน GitHub โดยเลือก Public
3. เลือก Add file → Upload files แล้วอัปโหลดไฟล์และโฟลเดอร์ทั้งหมดที่แตกออกมา
   ให้ index.html อยู่ระดับบนสุดของ repository และเก็บโฟลเดอร์ assets ไว้ตามเดิม
4. กด Commit changes
5. เปิด Settings → Pages → Build and deployment
6. เลือก Source: Deploy from a branch
7. เลือก Branch: main และโฟลเดอร์ / (root) แล้วกด Save
8. รอ GitHub เผยแพร่ แล้วเปิด URL ที่ปรากฏในหน้า Pages
   โดยทั่วไปจะเป็น https://ชื่อผู้ใช้.github.io/ชื่อ-repository/

## ข้อควรรู้

- ไม่ต้องติดตั้ง Node.js หรือสั่ง build
- อย่าเปลี่ยนชื่อหรือตำแหน่งไฟล์อ้างอิง เพราะเว็บใช้ relative paths รองรับ repository subpath
- หากต้องการชื่อหน้า insure_retire.html สามารถคัดลอก index.html แล้วตั้งชื่อเป็น insure_retire.html
  โดยเก็บ index.html ไว้ด้วยเพื่อให้ URL หลักเปิดได้
- การดับเบิลคลิกเปิด index.html ผ่าน file:// อาจโหลดข้อมูลไม่ได้ เนื่องจากใช้ JavaScript modules และ fetch
  ให้ทดสอบผ่าน GitHub Pages หรือ local HTTP server
- GitHub Pages ที่ตั้งเป็นสาธารณะเปิดให้ผู้มีลิงก์ใช้งานได้ และไฟล์ใน repository แบบ Public มองเห็นได้
- ปุ่ม LINE และข้อมูลติดต่อคงตามเว็บเวอร์ชันล่าสุด

## ไฟล์

index.html เป็นหน้าหลัก, style.css เป็นรูปแบบหน้าเว็บ, *.mjs เป็นการทำงานของเว็บ,
plans.json เป็นตารางอัตราเบี้ย, excel-template.json และ Flexi_Retire.xlsx เป็นไฟล์ประกอบ Excel,
assets/ เป็นฟอนต์และไลบรารี PDF ที่เว็บใช้งาน
