# Template: CDS Dashboard Report (ต้นฉบับ)

Template ที่ตรงกับ PDF output จริงของ CDS SCM Partner Service Dashboard
ใช้ร่วมกับ Style: `corporate_dark` (CDS SCM Default)

## Slides ทั้งหมด: 8 slides

| # | slide_id | ชื่อ | layout |
|---|---|---|---|
| 1 | cover | Dashboard Report | cover_purple_full |
| 2 | kpi | ภาพรวม KPI | kpi_5+5_cards |
| 3 | resolution | 1st Contact Resolution (FCR) | fcr_two_panel |
| 4 | dept | สรุป Case ทุกแผนก | dept_table |
| 5 | fcr_dept | FCR vs Non-FCR ตามแผนก | fcr_bar_chart |
| 6 | top10 | Top 10 Issue | top10_bar |
| 7 | res_time | Resolution Time ตามแผนก | resolution_bar |
| 8 | pending | Case ค้าง (Pending/Open) | pending_cards_table |

## Slide 1 — Cover

**Layout:** พื้นม่วงเต็ม + badge + title + KPI pills

KPI ที่แสดง: KPI Call, Mail, FCR (Call)%, FCR (Mail)%
Meta: ช่วงข้อมูล, วันที่สร้าง, Presented By

Narrative ใน output JSON:
```json
{
  "slide_id": "cover",
  "title": "DASHBOARD REPORT",
  "subtitle": "ช่วงข้อมูล: [period]",
  "kpi_pills": [
    {"label": "KPI Call", "value": "[totalCall]", "theme": "light_purple"},
    {"label": "Mail", "value": "[totalMail]", "theme": "light_purple"},
    {"label": "FCR (Call)", "value": "[fcrPct]%", "theme": "yellow"},
    {"label": "FCR (Mail)", "value": "[fmrPct]%", "theme": "light_purple2"}
  ]
}
```

## Slide 2 — ภาพรวม KPI

**Layout:** CALL section (5 cards) + MAIL section (5 cards)

CALL cards (สีตาม PDF):
1. Total Call — ม่วงอ่อน
2. FCR (Call) — ม่วง
3. Avg. Talk Time — ดำ (จาก 3CX)
4. Abandon Rate — แดง
5. Call Reach Rate — เขียว

MAIL cards:
1. Total Mail — ฟ้าอ่อน
2. FCR (Mail) — ฟ้า
3. Avg. Resolution (Call) — เหลือง
4. Avg. Resolution (Mail) — น้ำเงิน
5. Case ค้าง — แดง

## Slide 3 — FCR

**Layout:** 2 panel ซ้าย-ขวา เท่ากัน

ซ้าย: FCR Call — ตัวเลขใหญ่ + progress bar + status badge
ขวา: FCR Mail — ตัวเลขใหญ่ + progress bar + status badge

Status badge:
- ≥ 90%: "ดีมาก" เขียว ✅
- ≥ 85%: "On Target" เขียว ✅
- 80-84%: "พอใช้" เหลือง ⚠️
- < 80%: "ต่ำกว่าเป้า" แดง ❌

## Slide 4 — สรุปแผนก

**Layout:** ตาราง 6 columns

Columns: แผนก | Total | % | Call | Mail | FCR% | สถานะ
แถวสลับสี + progress bar ใน FCR column + icon status

## Slide 5 — FCR vs Non-FCR

**Layout:** Horizontal stacked bar chart

Bar: FCR (ฟ้า) + Non-FCR (แดง) + พื้น (ม่วงอ่อน)
Label: ชื่อแผนก ซ้าย + n/total + % ขวา

## Slide 6 — Top 10 Issue

**Layout:** Ranked horizontal bars

สีวนซ้ำ: ม่วง → ฟ้า → น้ำเงิน → เหลือง → เทา
ตัวเลข rank ซ้าย + label + bar + count + cumulative %

## Slide 7 — Resolution Time

**Layout:** Horizontal bars แสดง avg วัน

พื้น bar: เขียวอ่อน เต็มความกว้าง
ค่าบาร์: สีตาม threshold
Legend ล่าง: ≤0.5วัน / ≤1วัน / ≤3วัน / >3วัน

## Slide 8 — Case ค้าง

**Layout:** 3 metric cards + ตาราง

Cards: จำนวนค้าง (เหลือง) + Avg Pending (แดง) + Max Pending (ม่วง)
ตาราง: header เหลือง + แถวสลับ + status icon

## Narrative ที่ต้องการ

Claude ต้องสร้าง narrative สำหรับแต่ละ slide โดย:
- ภาษาไทย กระชับ ไม่เกิน 2-3 ประโยคต่อ slide
- ระบุตัวเลขจริง เปรียบเทียบกับเกณฑ์
- Slide 2 (KPI Overview): สรุปภาพรวม highlight จุดเด่น/จุดอ่อน
- Slide 3 (FCR): บอกสถานะและ gap จากเป้าหมาย
- Slide 8 (Pending): ระบุแผนกที่ต้องติดตาม

## Output JSON Schema

```json
{
  "template_used": "cds_dashboard_report",
  "style_used": "corporate_dark",
  "period": "ช่วงเวลา",
  "headline": "สรุป 1 ประโยค",
  "slides": [
    {
      "slide_id": "kpi",
      "narrative": "ข้อความบรรยายสำหรับ slide นี้"
    }
  ],
  "narrative_full": {
    "kpiSummary": "...",
    "strengths": "...",
    "concerns": "...",
    "recommendation": "..."
  }
}
```
