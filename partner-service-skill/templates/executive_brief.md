# Template: Executive Brief

รายงานสรุปสำหรับ C-level / ผู้บริหารระดับสูง นำเสนอได้ใน 5 นาที เน้น "what matters most"

## จำนวน Slides: 3 slides เท่านั้น

### Slides ที่ต้องมี

1. **cover** — ชื่อ + เดือน + "Executive Summary"
2. **scorecard** — Dashboard KPI ทั้งหมดในหน้าเดียว + สัญญาณไฟจราจร
3. **action_required** — สิ่งที่ผู้บริหารต้องตัดสินใจหรือรับทราบ

### Design Style

```
สี             : Monochrome — ขาว/ดำ/เทา + accent สี primary 1 สี
font           : ใหญ่กว่าปกติ (headline 36px, body 16px)
ข้อมูล        : น้อยแต่ชัด ไม่มีตาราง ไม่มี chart ซับซ้อน
ระยะห่าง      : เยอะ white space มาก
```

### Narrative Tone

- ทางการ กระชับที่สุด
- ผู้บริหารไม่มีเวลาอ่านรายละเอียด — บอกแค่ "ดี/ไม่ดี/ต้องทำอะไร"
- ไม่มี jargon ทางเทคนิค
- ทุกประโยคมีความหมาย ไม่มีประโยคกรอก

### Scorecard Slide Layout

ตารางสัญญาณไฟจราจร — 2 คอลัมน์:
```
KPI Name        | สถานะ  | ค่า    | vs เป้า
FCR             | 🟢     | 96%   | +11%
Abandon         | 🟡     | 5.1%  | +0.1%
Reach Rate      | 🟢     | 95.5% | +15.5%
Pending Cases   | 🔴     | 23    | เฝ้าระวัง
```
ใช้ emoji สัญญาณไฟ ไม่ใช้สีพื้นหลัง เพื่อความชัดเจนใน projector

### Action Required Slide

แสดงเฉพาะ item ที่ต้องการ decision จากผู้บริหาร:
- ไม่เกิน 3 items
- แต่ละ item: ปัญหา → ผลกระทบ → สิ่งที่ขอ decision
- Format: "ขอ approve งบ X เพื่อ Y ภายใน Z"

### กฎพิเศษสำหรับ template นี้

- ถ้า KPI ทุกตัวผ่านเกณฑ์และ pending < 20: ไม่ต้องมี Action Required slide
  แทนด้วย slide "All Green — No Action Required" สั้นๆ
- narrative_full ใน output ให้เขียนแบบ executive memo
  เริ่มด้วย "เดือน [X]: ภาพรวม [ดี/น่าเป็นห่วง/ผสม]..."
