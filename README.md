# Solo DnD Engine

เว็บเล่น DnD 5e คนเดียวโดยมี AI เป็น Dungeon Master ใช้ Gemini API รันบนเบราว์เซอร์ล้วน (ไฟล์ HTML ไฟล์เดียว ไม่มี backend)

## ฟีเจอร์
- ชีตตัวละคร (HP, AC, Speed, Pride), ไอเทม, สหายปาร์ตี้, Lore และบุคลิก
- ทอยเต๋า d4–d20 รองรับ Advantage และ Critical
- DM เสนอชอยส์พร้อมค่า DC หรือพิมพ์การกระทำอิสระได้
- Short Rest / Long Rest, แต้ม Pride
- บันทึกตัวละครและเนื้อเรื่องในเบราว์เซอร์ (localStorage)
- ใช้ได้ทั้ง PC และมือถือ

## วิธีใช้งานผ่าน GitHub Pages
1. สร้าง repository ใหม่บน GitHub แล้วอัปโหลด `index.html` และ `README.md`
2. ไปที่ **Settings → Pages**
3. ที่ **Build and deployment** เลือก Source เป็น **Deploy from a branch**
4. เลือก branch `main` โฟลเดอร์ `/ (root)` แล้วกด Save
5. รอสักครู่ เว็บจะอยู่ที่ `https://<ชื่อผู้ใช้>.github.io/<ชื่อ repo>/`

หรือดาวน์โหลด `index.html` ไปเปิดในเบราว์เซอร์ตรงๆ ก็ใช้ได้

## ตั้งค่า API Key
1. ขอ API Key ที่ [Google AI Studio](https://aistudio.google.com/apikey)
2. เปิดเว็บ กดปุ่ม **ตั้งค่า API / โมเดล** วาง Key แล้วกดบันทึก
3. ถ้าชื่อโมเดลใช้ไม่ได้ (ขึ้น 404) ให้พิมพ์ชื่อโมเดลที่ถูกต้องในช่องโมเดล ตรวจรายชื่อได้ที่ docs ของ Google

## ความปลอดภัย
- API Key เก็บใน localStorage ของเบราว์เซอร์คุณเท่านั้น **ไม่อยู่ในโค้ด** จึงไม่ถูกอัปขึ้น GitHub
- อย่าเขียน Key ลงในไฟล์ `index.html` ก่อน commit
- ใช้เฉพาะบนเครื่องที่ไว้ใจได้ และควรตั้งโควตา/จำกัดการใช้งาน Key ใน Google AI Studio

## หมายเหตุ
- ข้อมูลเซฟผูกกับเบราว์เซอร์และอุปกรณ์ ไม่ข้ามเครื่อง
- ล้างข้อมูลเบราว์เซอร์จะทำให้เซฟหาย
