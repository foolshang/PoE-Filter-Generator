# PoE Filter Generator (PoE1 & PoE2)

เครื่องมือสร้าง **loot filter** สำหรับ Path of Exile 1 และ 2 แบบ standalone —
ไฟล์เดียว ไม่ต้องติดตั้ง ไม่ต้องลง Python

รองรับทั้ง **PoE1** และ **PoE2** สลับได้ในหน้าต่างเดียว

---

## โหลด

👉 **[ดาวน์โหลดตัวล่าสุด (PoE-Filter-Generator.exe)](https://github.com/foolshang/PoE-Filter-Generator/releases/latest/download/PoE-Filter-Generator.exe)**

หรือเข้าหน้า [Releases](https://github.com/foolshang/PoE-Filter-Generator/releases) เพื่อเลือกเวอร์ชัน

> **Windows เท่านั้น** · ไฟล์เดียวจบ ดับเบิลคลิกรันได้เลย

### ครั้งแรกที่รัน Windows อาจเตือน
ไฟล์ไม่ได้ sign ดิจิทัล → Windows SmartScreen จะขึ้น "Windows protected your PC"
กด **More info → Run anyway** ครั้งเดียว ครั้งต่อไปไม่ถามอีก

---

## ใช้ยังไง

1. เปิดโปรแกรม → เลือกภาค **PoE1 / PoE2** ด้านบน
2. ตั้งค่า filter ที่ต้องการ (ดู 2 โหมดด้านล่าง)
3. ตั้ง **Game folder** (เว้นว่าง = หาโฟลเดอร์เกมให้อัตโนมัติ)
4. กด **Generate Now**
5. ในเกม: **Options → Game → เลือก filter แล้ว reload**

### 2 โหมด

**โหมดปกติ (tier ตามราคา)**
สร้างจาก NeverSink base filter (S/A/B/C)
ปรับ **Strictness** และเสียงแจ้งเตือนได้

**โหมดโชว์เฉพาะ (Whitelist)** — ติ๊ก "โหมดโชว์เฉพาะ"
โชว์เฉพาะที่เลือก **ซ่อนที่เหลือทั้งหมด**:
- **Currency** (Divine / Mirror / Exalted / Chaos / Regal / Vaal / Annulment)
- **Gold**
- **หมวด** (Rune, Essence, Fragment ฯลฯ) — เลือกตัดบางรายการในหมวดได้
- **ชื่อที่พิมพ์เอง** — พิมพ์ชื่อ base (เช่น `heavy belt`) + เลือก rarity (Normal/Magic/Rare/Unique) ต่อชื่อ
- **Gem**
  - PoE2: ติ๊ก Uncut Skill / Support / Spirit Gem + กำหนด level ขั้นต่ำ
  - PoE1: พิมพ์ชื่อ gem (มี autocomplete) เพิ่มได้หลายตัว

---

## ต้องมีอะไร

- Windows 10/11
- Path of Exile 1 หรือ 2 (ติดตั้งแล้ว)
- อินเทอร์เน็ต (ดึงราคา/base filter ตอน generate)

---

## แก้ปัญหา

**Generate แล้วขึ้น error เขียนไฟล์ไม่ได้ (เช่น `[Errno 9]` / Bad file descriptor)**
สาเหตุที่พบบ่อยคือ **Windows Defender "Controlled Folder Access"** (ระบบกัน ransomware)
บล็อกไม่ให้โปรแกรมหน้าใหม่เขียนไฟล์ลงโฟลเดอร์ Documents / My Games วิธีแก้:
1. Windows Security → **Virus & threat protection** → **Ransomware protection** →
   **Controlled folder access** → **Allow an app through Controlled folder access** →
   เพิ่ม `PoE-Filter-Generator.exe`
2. หรือกด **Browse...** ที่ช่อง *Game folder override* ในโปรแกรม แล้วเลือกโฟลเดอร์
   filter ของเกมเอง (โฟลเดอร์ที่ไม่ถูกบล็อก)

> ค่าเริ่มต้นของ Windows คือ "ปิด" CFA — ส่วนใหญ่จะไม่เจอปัญหานี้ แต่ถ้าคุณเปิดไว้ ใช้วิธีด้านบน

---

## หมายเหตุ

- โหมดปกติต่อยอดจาก **[NeverSink Filter](https://github.com/NeverSinkDev/NeverSink-Filter)** (เครดิต NeverSink)
- โปรแกรมนี้**ไม่มีส่วนเกี่ยวข้อง**กับ Grinding Gear Games
- filter ที่สร้างจะเขียนทับไฟล์ในโฟลเดอร์ filter ของเกม — ตรวจชื่อไฟล์ก่อนถ้ามี filter เดิมอยู่

---

*เป็นเครื่องมือส่วนตัวแจกให้ใช้ฟรี — เจอบั๊กหรืออยากได้อะไรเพิ่ม แจ้งได้ที่หน้า Issues*
