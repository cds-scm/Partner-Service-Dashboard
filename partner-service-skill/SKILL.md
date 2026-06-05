---
name: partner-service-pptx
description: สร้าง PowerPoint presentation สำหรับ CDS SCM Partner Service Call Center จาก KPI snapshot data ใช้เมื่อต้องการ export รายงาน PPTX, สร้าง monthly report, วิเคราะห์ KPI call center, เขียน narrative ภาษาไทย, หรือสร้าง slide deck สำหรับประชุมหรือรายงานผู้บริหาร ให้ใช้ skill นี้ทุกครั้งที่มีคำว่า Export PPTX, Monthly Report, KPI Report, Partner Service, Call Log, FCR, Abandon, หรือต้องการ presentation จาก dashboard data
---

# Partner Service PPTX Skill

สร้าง presentation คุณภาพสูงสำหรับทีม Partner Service CDS SCM โดยวิเคราะห์ KPI และเขียน narrative ภาษาไทยที่กระชับ อ่านง่าย เหมาะสำหรับประชุมและรายงานผู้บริหาร

## ขั้นตอนการทำงาน

1. อ่าน KPI snapshot ที่ได้รับ
2. เลือก template ตาม `template_type` ที่ระบุ (ดูรายละเอียดใน `templates/` folder)
3. วิเคราะห์ตาม `custom_focus` ถ้ามี
4. ส่งกลับ JSON ตาม output schema ด้านล่าง

## Styles ที่มี

อ่านไฟล์ style ที่เลือกก่อนทำงานทุกครั้ง เพื่อใช้ colors ที่ถูกต้อง:

| style_id | ไฟล์ | ใช้เมื่อ |
|---|---|---|
| `corporate_dark` | `styles/corporate_dark.md` | Board meeting, รายงาน C-level (default) |
| `fresh_teal` | `styles/fresh_teal.md` | Weekly standup, Team meeting |
| `minimal_light` | `styles/minimal_light.md` | Print, แชร์ทาง email |
| `bold_purple` | `styles/bold_purple.md` | รายงานภายในองค์กร CDS brand |
| `dynamic_purple` | `styles/dynamic_purple.md` | Presentation ที่ต้องการ visual impact สูง, Client presentation |

ถ้าไม่ระบุ `style_id` ให้ใช้ `corporate_dark` เป็น default

## Templates ที่มี

อ่านไฟล์ template ที่เลือกก่อนทำงานทุกครั้ง:

| template_type | ไฟล์ | ใช้เมื่อ |
|---|---|---|
| `cds_dashboard_report` | `templates/cds_dashboard_report.md` | **Default** — ตรงกับ PDF output จริง 8 slides |
| `monthly_report` | `templates/monthly_report.md` | รายงานประจำเดือน ผู้บริหาร |
| `weekly_summary` | `templates/weekly_summary.md` | สรุปรายสัปดาห์ ทีมงาน |
| `executive_brief` | `templates/executive_brief.md` | สรุปสั้น C-level 5 นาที |

ถ้าไม่ระบุ `template_type` ให้ใช้ `cds_dashboard_report` เป็น default

## KPI Thresholds (เกณฑ์มาตรฐาน)

```
FCR (Call)        : เป้า ≥ 85%   | ดีมาก ≥ 90% | ต่ำ < 80%
FMR (Mail)        : เป้า ≥ 80%   | ดีมาก ≥ 85% | ต่ำ < 75%
Abandon Rate      : เป้า ≤ 5%    | ดี ≤ 3%     | สูง > 8%
Call Reach Rate   : เป้า ≥ 80%   | ดี ≥ 90%    | ต่ำ < 75%
Avg Resolution    : เป้า ≤ 1 วัน  | ดี ≤ 0.5วัน | ช้า > 2 วัน
Pending Cases     : เฝ้าระวัง > 20 | วิกฤต > 50
```

## Status Color Rules

```
green  (#059669) : ผ่านเกณฑ์ หรือ ดีกว่าเป้า
amber  (#D97706) : ใกล้เป้า (±5%)
red    (#DC2626) : ต่ำกว่าเกณฑ์
```

## Narrative Style Guide

- ภาษาไทย กระชับ ประโยคไม่เกิน 2 บรรทัด
- เริ่มด้วย headline 1 ประโยค บอกภาพรวมทันที
- ใช้ตัวเลขจริง ไม่ใช้คำกว้างๆ เช่น "ดีขึ้น" → "เพิ่มขึ้น 3%"
- จุดแข็ง: ระบุตัวเลขที่เด่น + เหตุผลสั้นๆ
- จุดปรับปรุง: ระบุปัญหา + ผลกระทบ + แนวทาง
- คำแนะนำ: Actionable ทำได้จริง ระบุแผนก/ผู้รับผิดชอบถ้าทำได้
- ห้ามใช้ภาษาทางการแข็งๆ เช่น "อนึ่ง", "ดังนั้น" — ใช้ภาษาปกติ

## Input Schema (KPI Snapshot)

```json
{
  "template_type": "monthly_report | weekly_summary | executive_brief",
  "custom_focus": "โจทย์พิเศษ เช่น เน้นแผนก FAST หรือ เปรียบเทียบกับเดือนก่อน",
  "period": "May 2026",
  "totalCall": 862,
  "totalMail": 432,
  "fcrPct": 96,
  "fmrPct": 85,
  "abandonPct": 5.1,
  "callReachRatePct": 95.5,
  "avgTalkTime": "4:32",
  "avgResolutionCall": 0.1,
  "avgResolutionMail": 0.2,
  "pendingCases": 23,
  "c2TransferPct": 4,
  "over7Days": 5,
  "over14Days": 2,
  "topDepts": "ASN/EDI:312, FAST:198, DC:145",
  "top3Issues": "EDI Password Reset:45, ASN Upload Error:38, FAST B2P:29",
  "trendFCR": "+1%",
  "trendAbandon": "+2%",
  "trendCall": "-5%"
}
```

## Output Schema

ส่งกลับ JSON เท่านั้น ไม่มีข้อความอื่น ไม่มี markdown code block:

```json
{
  "template_used": "monthly_report",
  "style_used": "corporate_dark",
  "theme": {
    "header_bg": "1E1B3A",
    "header_text": "FFFFFF",
    "accent": "FCD34D",
    "primary": "6C5CE7",
    "primary_light": "EDE9FE",
    "body_bg": "FFFFFF",
    "body_bg2": "F9FAFB",
    "text_dark": "111827",
    "text_gray": "6B7280",
    "border": "E5E7EB",
    "status_green": "059669",
    "status_amber": "D97706",
    "status_red": "DC2626"
  },
  "headline": "ประโยคสรุปภาพรวม ≤ 80 ตัวอักษร",
  "slides": [
    {
      "slide_id": "cover",
      "title": "ชื่อ slide",
      "subtitle": "ช่วงเวลา หรือ tagline",
      "layout": "cover"
    },
    {
      "slide_id": "kpi_overview",
      "title": "ภาพรวม KPI",
      "layout": "kpi_grid",
      "kpis": [
        {
          "label": "FCR",
          "value": "96%",
          "sub": "830/862 สาย",
          "status": "green",
          "trend": "+1%"
        }
      ],
      "narrative": "ข้อความบรรยาย KPI ในสไลด์นี้"
    },
    {
      "slide_id": "strengths_concerns",
      "layout": "two_column",
      "left": {
        "heading": "จุดแข็ง",
        "bullets": ["bullet 1", "bullet 2"]
      },
      "right": {
        "heading": "จุดที่ต้องปรับ",
        "bullets": ["bullet 1", "bullet 2"]
      }
    },
    {
      "slide_id": "recommendation",
      "layout": "action_items",
      "title": "คำแนะนำ",
      "items": [
        {
          "priority": "high | medium | low",
          "action": "สิ่งที่ต้องทำ",
          "owner": "แผนก/ทีม",
          "timeline": "ระยะเวลา"
        }
      ]
    }
  ],
  "narrative_full": {
    "kpiSummary": "สรุป KPI 2-3 ประโยค",
    "strengths": "จุดแข็ง 1-2 ประโยค",
    "concerns": "จุดที่ควรปรับปรุง 1-2 ประโยค",
    "recommendation": "คำแนะนำ 1-2 ประโยค"
  }
}
```

## ข้อห้าม

- ห้ามส่งข้อความนอก JSON
- ห้ามใส่ markdown code block (``` ) ล้อม JSON
- ห้ามคิดค้น KPI ที่ไม่มีใน input
- ถ้า KPI ไม่มีข้อมูล ให้ใส่ `null` และ `status: "gray"`
- narrative ต้องอิงตัวเลขจริงจาก input เท่านั้น
