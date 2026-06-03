# 🎰 Gacha Drop Rate Simulator

เว็บจำลองอัตราดรอปกาชา (single-file web app) — เปิด `index.html` ในเบราว์เซอร์ได้ทันที ไม่ต้องติดตั้งอะไร

## ฟีเจอร์
1. **Rate Setting** — ตั้งเรท SSR / SR / R / N (รวมต้อง = 100%) พร้อมปุ่ม Normalize
2. **Item Pool Management** — เพิ่ม/แก้/ลบ item เลือก rarity ได้ + empty state
3. **Single Simulation** — สุ่มตามเรทจริง กรอกจำนวนครั้ง + ราคาต่อครั้ง
4. **Result Display** — Summary, breakdown table, item results, ค่าใช้จ่าย, rarity ที่ออกมากสุด
5. **Export CSV** — ผล single sim และ Player POV summary
6. **Validation** — ตรวจเรท, input, item pool
7. **Player POV Monte Carlo** — กรอกงบ ดูโอกาสได้ SSR / item, chance กาชาแห้ง (0 SSR), best/worst
8. **Free Roll Rule** — สุ่มครบ X ครั้งได้ฟรี Y ครั้ง (นับจาก paid เท่านั้น)
9. **Pity / History / Chart / Insight** — ระบบ pity การันตี, ประวัติ, กราฟ, insight ภาษาคน

นอกจากนี้มีแท็บ **📝 Prompt Log** บันทึก prompt ที่ใช้พัฒนาแอป

## การใช้งาน
เปิด `index.html` หรือเข้าผ่าน GitHub Pages (ถ้าเปิดใช้งาน)

## เทคโนโลยี
HTML + Vanilla JS + Chart.js (CDN) · ไฟล์เดียวจบ
