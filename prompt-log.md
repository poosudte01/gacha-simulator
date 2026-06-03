# 📝 Prompt Log — Gacha Drop Rate Simulator

บันทึก **prompt ต้นฉบับทั้งหมด** ของ task นี้ (คำต่อคำ) พร้อมสรุปสิ่งที่ทำในแต่ละรอบ

---

### #1 · 2026-06-03
**Prompt (ต้นฉบับ):**
> ช่วยสร้างเว็บจำลองกาชา Gacha Drop Rate Simulator ให้หน่อยโดยมีเงื่อนไขดังนี้
> 1. Rate Setting — ตั้งค่า Rate ของ SSR / SR / R / N ได้ และ Rate รวมต้องเท่ากับ 100%
> 2. Item Pool Management — เพิ่มรายชื่อ Item/ตัวละคร เลือก Rarity ได้ มีปุ่ม + Add Item และลบ/แก้ไขได้
> 3. Single Simulation — กรอกจำนวนครั้งสุ่มและราคาต่อครั้ง แล้วสุ่มผลลัพธ์ตาม Rate จริง
> 4. Result Display — แสดง Summary, Table, Item Result, ค่าใช้จ่าย และ Rarity ที่ออกมากที่สุด
> 5. Export CSV — Export ผลลัพธ์ล่าสุดและ Player POV Summary เป็น CSV ได้
> 6. Validation — ตรวจ rate, input, item pool และค่าที่ผิดชัดเจน
> 7. Player POV Simulator — กรอกงบเติมเงิน แล้วจำลอง Monte Carlo เพื่อดูโอกาสได้ SSR/Item
> 8. Free Roll Rule — ตั้งค่าสุ่มครบ X ครั้ง ได้สุ่มฟรี Y ครั้ง โดยนับจาก paid rolls เท่านั้น
> 9. Pity / History / Chart — ระบบ pity, history, chart, insight
> โดยใช้สกิลที่เกี่ยวข้องในโฟลเดอร์ Claude Skill Ultimate Bundle

**สิ่งที่ทำ:** สร้าง `gacha-simulator.html` เป็น single-file web app ครบทั้ง 9 ฟีเจอร์ แบ่ง 3 แท็บ (ตั้งค่า & Pool / Single Simulation / Player POV) ทดสอบ logic ใน sandbox — การกระจายตรงเรท (3/12/35/50%), free roll นับจาก paid เท่านั้น, pity การันตี SSR

---

### #2 · 2026-06-03
**Prompt (ต้นฉบับ):**
> ต้องแสดง chance 0 SSR และมี best/worst SSR result ด้วย และภาษาต้องอ่านแล้วเป็นมนุษย์

**สิ่งที่ทำ:** เพิ่ม KPI โอกาสกาชาแห้ง (0 SSR), 🍀 ดวงดีสุด / 💀 ดวงร้ายสุด, SSR ที่เจอบ่อยสุด (mode); เขียน insight ใหม่ให้เป็นภาษาคน; เพิ่มค่าลง CSV; ตรวจสอบ P(≥1 SSR)+P(0 SSR)=100%

---

### #3 · 2026-06-03
**Prompt (ต้นฉบับ):**
> เพิ่ม empty state ตอน item pool ว่างด้วย

**สิ่งที่ทำ:** แสดงกล่อง placeholder (📦 "ยังไม่มี item ในกล่องสุ่ม") แทนตารางเปล่าเมื่อ pool ว่าง

---

### #4 · 2026-06-03
**Prompt (ต้นฉบับ):**
> อยากให้สามารถ Reset history ได้

**สิ่งที่ทำ:** เพิ่มปุ่ม 🧹 ล้าง History ในการ์ด History; เคลียร์ประวัติแล้วแสดง empty state โดย Summary/Chart ยังอยู่

---

### #5 · 2026-06-03
**Prompt (ต้นฉบับ):**
> ขอ Prompt Log ด้วย

**สิ่งที่ทำ:** สร้างไฟล์ `prompt-log.md` และฝัง Prompt Log เป็นแท็บที่ 4 ในตัวแอป

---

### #6 · 2026-06-03
**Prompt (ต้นฉบับ):**
> Prompt Log ทั้งหมดของ Task นี้นะ

**สิ่งที่ทำ:** ปรับ Prompt Log ให้บันทึก prompt ต้นฉบับแบบเต็ม (คำต่อคำ) ครบทุกข้อของ task ทั้งในไฟล์ md และในแท็บของแอป

---

## หมายเหตุ
- ไฟล์หลัก: `gacha-simulator.html` — เปิดด้วยเบราว์เซอร์ได้ทันที ไม่ต้องติดตั้งอะไร
- CSV ที่ export ได้: `gacha_sim_result.csv` (single sim) และ `gacha_player_pov.csv` (Player POV Monte Carlo)
- Prompt Log ฉบับนี้อัปเดตทุกครั้งที่มีการเพิ่ม/แก้ฟีเจอร์
