# Style: CDS SCM Default ★ (ต้นฉบับจริง)

สไตล์ที่ใช้จริงใน CDS SCM Partner Service Dashboard
อ้างอิงจาก PDF output วันที่ 05 มิถุนายน 2569

## Colors

```json
{
  "style_id": "corporate_dark",
  "header_bg": "1E1B3A",
  "header_text": "FFFFFF",
  "accent": "FCD34D",
  "accent_dark": "F59E0B",
  "primary": "7C3AED",
  "primary_light": "EDE9FE",
  "body_bg": "FFFFFF",
  "body_bg2": "F9FAFB",
  "text_dark": "111827",
  "text_gray": "6B7280",
  "text_light": "FFFFFF",
  "border": "E5E7EB",
  "status_green": "10B981",
  "status_amber": "F59E0B",
  "status_red": "EF4444",
  "status_blue": "2563EB",
  "teal": "0EA5E9",
  "call_card_1": "EDE9FE",
  "call_card_2": "7C3AED",
  "call_card_3": "1E1B3A",
  "call_card_4": "EF4444",
  "call_card_5": "10B981",
  "mail_card_1": "DBEAFE",
  "mail_card_2": "0EA5E9",
  "mail_card_3": "F59E0B",
  "mail_card_4": "2563EB",
  "mail_card_5": "EF4444"
}
```

## Design Rules — ดูจาก PDF จริง

### Brand Bar (Header)
- พื้น: `1E1B3A` ดำเข้ม ความสูง 0.42 นิ้ว
- เส้นซ้าย: `FCD34D` เหลือง 0.06 นิ้ว
- ข้อความ "Partner Service": ขาว bold 8.5px ซ้าย
- Yellow circle ขวาสุด: `FCD34D` ขนาด 0.34 นิ้ว
- Dot grid (2×3) ก่อน circle: `A78BFA` ม่วงอ่อน

### Title Bar
- เส้นซ้าย accent: `7C3AED` ม่วง
- พื้น: `FAFAFA` ขาวอมเทา
- Title text: `111827` ดำเข้ม bold 18px

### Page Number Badge (มุมขวาล่างทุก slide)
- Background: `1E1B3A` ดำ
- ตัวเลข: ขาว
- วงกลมม่วง: `7C3AED` ด้านขวาของ badge

### Footer
- แถบ: `1E1B3A` ดำ ความสูง 0.245 นิ้ว
- ข้อความ: ขาว 8px "CDS SCM Partner Service · วันที่ · ข้อมูล X รายการ"
- Yellow circle ขวา: `FCD34D`

## Cover Slide (Slide 1)

```
พื้นหลัง: #7C3AED ม่วง
Badge ซ้ายบน: เหลือง #FCD34D pill — "CDS SCM  Partner Service"
Stars: ✶ สีเหลือง 2 ข้าง badge
Dot grid: ม่วงอ่อน 3×4 ขวากลาง
Yellow circle solid: ขวาบน ใหญ่

Title: "DASHBOARD" ขาว bold ใหญ่มาก ซ้าย
       "REPORT" เหลือง #FCD34D bold ใหญ่มาก ซ้าย

เส้น divider: เทา horizontal

KPI pills 4 ใบ เรียงแถว เต็มความกว้าง:
  1. KPI Call  — พื้น EDE9FE (ม่วงอ่อน), ตัวเลข 7C3AED
  2. Mail      — พื้น EDE9FE (ม่วงอ่อน), ตัวเลข 7C3AED
  3. FCR Call  — พื้น FCD34D เหลือง, ตัวเลข ดำ 111827
  4. FCR Mail  — พื้น E9E2FF (ม่วงอ่อนมาก), ตัวเลข 7C3AED

Meta ล่างซ้าย: Yellow circle เล็ก + "Generated: วันที่" + "Presented By: Partner Service Team"
```

## KPI Overview Slide (Slide 2)

### CALL Section
```
Section label "CALL": 7C3AED ม่วง letter-spacing กว้าง
5 cards แถวเดียว เต็มความกว้าง ขนาดเท่ากัน:
  1. Total Call  — EDE9FE ม่วงอ่อน, ตัวเลข 7C3AED
  2. FCR (Call)  — 7C3AED ม่วง, ตัวเลข+label ขาว
  3. Avg Talk    — 1E1B3A ดำ, ตัวเลข+label ขาว
  4. Abandon     — EF4444 แดง, ตัวเลข+label ขาว
  5. Reach Rate  — 10B981 เขียว, ตัวเลข+label ขาว
```

### MAIL Section
```
Section label "MAIL": 0EA5E9 ฟ้า letter-spacing กว้าง
5 cards แถวเดียว:
  1. Total Mail        — DBEAFE ฟ้าอ่อน, ตัวเลข 0EA5E9
  2. FCR (Mail)        — 0EA5E9 ฟ้า, ตัวเลข ขาว
  3. Avg Res (Call)    — F59E0B เหลือง, ตัวเลข ขาว
  4. Avg Res (Mail)    — 2563EB น้ำเงิน, ตัวเลข ขาว
  5. Case ค้าง (Pending) — EF4444 แดง, ตัวเลข ขาว
```

## FCR Slide (Slide 3)
```
2 panel ซ้าย-ขวา:
  ซ้าย: header เขียว #10B981, ตัวเลข 96% ใหญ่มาก ดำ
        Progress bar เขียว + badge "ดีมาก" เขียว
  ขวา:  header เขียวอมฟ้า #0EA5E9 (ม่วง #7C3AED ถ้า FMR)
        ตัวเลข 83% ใหญ่มาก ดำ
        Progress bar เหลือง + badge "พอใช้" เหลือง
```

## Dept Summary Slide (Slide 4)
```
Table header: 7C3AED ม่วง, ข้อความขาว
แถวสลับ: ขาว / EDE9FE (ม่วงอ่อน)
FCR column: ตัวเลขสีตาม threshold (เขียว/เหลือง/แดง)
Status: icon ✅ + ข้อความสี / ⚠️ + ข้อความสี
Progress bar: เขียว #10B981 ส่วน Level1, เทา ส่วนที่เหลือ
```

## FCR vs Non-FCR Slide (Slide 5)
```
Bar แนวนอนเต็มความกว้าง:
  Level 1 (FCR): 0EA5E9 ฟ้า-เขียว
  Level 2 (Non-FCR): EF4444 แดง
  พื้น bar: EDE9FE (ม่วงอ่อน) — ส่วนที่เหลือ
ตัวเลข n/total และ % สีเขียว/เหลือง/แดงตาม threshold
```

## Top 10 Issue Slide (Slide 6)
```
Bar สีต่างกันตามลำดับ cycling:
  1-2: 7C3AED ม่วง
  3-4: 0EA5E9 ฟ้า
  5-6: 2563EB น้ำเงิน
  7-8: F59E0B เหลือง
  9-10: 6B7280 เทา
Bar มีตัวเลขในบาร์ (ขาว)
Cumulative % ขวา: เทา
```

## Resolution Time Slide (Slide 7)
```
Horizontal bar แบบ gradient:
  ≤ 0.5 วัน: 0EA5E9 ฟ้า (เต็มสีสว่าง)
  ≤ 1 วัน:   10B981 เขียว
  ≤ 3 วัน:   F59E0B เหลือง
  > 3 วัน:   EF4444 แดง
พื้น bar: E8F5E9 เขียวอ่อนมาก
ตัวเลขวัน: ขาว อยู่ในบาร์
จำนวน case: เทา ขวาบาร์
```

## Pending Cases Slide (Slide 8)
```
3 metric cards ด้านบน:
  Case ค้างทั้งหมด: F59E0B เหลือง
  Avg Pending Time: EF4444 แดง
  Max Pending Time: 7C3AED ม่วง
Table header: F59E0B เหลือง, ข้อความดำ
แถว: สลับ ขาว / FFF8F0 (เหลืองอ่อนมาก)
Status: ⚠️ ต้องติดตาม สีเหลือง / ✅ ปกติ สีเขียว
```

## Typography
```
Font: CPN (ภาษาไทย), Inter/Helvetica (fallback)
Header bar: 8.5px bold
Title: 18-20px bold
KPI ตัวเลขใหญ่: 28-42px bold
KPI label: 9-10px
Body text: 11-12px
Footer: 8px
```

## Mood & Usage
ใช้เป็น default style สำหรับ CDS SCM Partner Service ทุก report
สมดุลระหว่าง professional (header สีเข้ม) กับ data-driven (KPI cards สีสด)
