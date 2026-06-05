# Style: Dynamic Purple

สไตล์สดใส ทันสมัย ม่วงสดตัดกับเหลืองทอง มีลวดลาย circle decorations มุมทั้งสี่ 
ได้แรงบันดาลใจจาก Monthly KPI Performance Report — Dynamic Agency
เหมาะสำหรับ presentation ที่ต้องการ impact สูง ดูน่าตื่นเต้น

## Colors

```json
{
  "style_id": "dynamic_purple",
  "header_bg": "8B5CF6",
  "header_text": "FFFFFF",
  "accent": "F59E0B",
  "accent_dark": "D97706",
  "primary": "7C3AED",
  "primary_light": "EDE9FE",
  "body_bg": "FFFFFF",
  "body_bg2": "FAF5FF",
  "text_dark": "1F2937",
  "text_gray": "6B7280",
  "text_light": "FFFFFF",
  "border": "DDD6FE",
  "cover_bg": "8B5CF6",
  "cover_overlay": "7C3AED",
  "status_green": "10B981",
  "status_amber": "F59E0B",
  "status_red": "EF4444",
  "status_blue": "3B82F6",
  "circle_deco": "FFFFFF"
}
```

## Design Rules

### Cover Slide
- พื้นหลัง: gradient ม่วง `8B5CF6` ทั้ง slide พร้อม overlay รูปภาพ opacity 40%
- ชื่อรายงาน: ขาว bold ใหญ่มาก (36-46px) กลาง slide
- Badge บริษัท: พื้น `F59E0B` เหลืองทอง ข้อความ `7C3AED` ม่วงเข้ม rounded pill
- ดาว asterisk (✶) สีเหลือง 2 ข้างของ badge
- Circle arcs: มุมขวาบนและซ้ายล่าง — วงกลมเส้นขาว stroke 2px opacity 30%
- เลขหน้า: มุมขวาล่าง

### Content Slides (หน้าเนื้อหา)
มี 2 pattern สลับกัน:

**Pattern A — Dark left strip:**
- แถบซ้าย: `1F2937` ดำเข้ม ความกว้าง 8% 
- บริษัท: badge มุมบนซ้ายบน dark strip ข้อความขาว
- เนื้อหา: พื้นขาวด้านขวา หัวข้อสีม่วง `7C3AED` bold
- Circle arcs: มุมขวาบน เส้น `DDD6FE` opacity 20%
- เลข PAGE: badge ดำ + วงกลมม่วง มุมขวาล่าง

**Pattern B — Purple accent:**
- พื้นหลัง: `8B5CF6` ม่วงทั้ง slide (สำหรับ slide ที่เน้น impact)
- ข้อความ: ขาวทั้งหมด
- ข้อมูล: badges ม่วงเข้ม/เขียว/น้ำเงิน บน card ขาว

### KPI Cards (ใน content slides)
- Card พื้น: `F3F0FF` ม่วงอ่อนมาก border `DDD6FE`
- Label badge: พื้น `7C3AED` ข้อความขาว rounded pill
- ตัวเลขหลัก: `1F2937` ดำ bold ใหญ่
- Progress bar: สูง 6px rounded กว้าง 100%
  - Achieved: `10B981` เขียว
  - Warning: `F59E0B` เหลือง
  - Below: `EF4444` แดง

### Section Headers (ใน slide)
- ข้อความหัวข้อ: `7C3AED` ม่วง bold italic
- ขนาด: 24-32px

### Footer
- แถบล่าง: `8B5CF6` ม่วง
- Badge "PAGE": พื้น `1F2937` ดำ + วงกลม `F59E0B` เหลือง

## Decoration Elements

วาดด้วย pptxgenjs `addShape(pptx.shapes.OVAL)`:

```
Circle arcs มุมขวาบน:
  - วงกลม 1: x=8.8, y=-0.8, w=2.5, h=2.5, fill=none, line={color:'FFFFFF', width:2, transparency:70}
  - วงกลม 2: x=9.2, y=-0.4, w=2.0, h=2.0, fill=none, line={color:'FFFFFF', width:1.5, transparency:70}

Circle arcs มุมซ้ายล่าง:
  - วงกลม 1: x=-1.2, y=4.2, w=2.5, h=2.5, fill=none, line={color:'FFFFFF', width:2, transparency:70}
  - วงกลม 2: x=-0.8, y=4.6, w=2.0, h=2.0, fill=none, line={color:'FFFFFF', width:1.5, transparency:70}
```

## Mood

สดใส พลังงานสูง ทันสมัย เหมาะกับ:
- Monthly KPI Report ที่ต้องการ visual impact
- Presentation ต่อ client หรือ stakeholder ภายนอก
- งาน showcase ผลงาน

## Layout ที่ใช้บ่อย

| layout_id | description |
|---|---|
| `cover_full` | Cover เต็ม slide พื้นม่วง |
| `split_dark` | ซ้ายดำ + ขวาขาว มีรูปซ้าย |
| `split_purple` | ซ้ายรูป + ขวาขาว หัวข้อม่วง |
| `full_purple` | พื้นม่วงทั้ง slide สำหรับ KPI overview |
| `card_grid` | ตารางการ์ด KPI 2-3 ใบ |
| `closing` | Cover ปิด เหมือน cover แต่ข้อความ Thank You |
