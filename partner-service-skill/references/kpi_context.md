# KPI Context — Partner Service CDS SCM

## เกี่ยวกับทีม

- ทีม Partner Service ดูแล Call Center สำหรับ Partner ของ CDS SCM
- แบ่งงานเป็น 2 ส่วน: Analysis และ Partner Service
- ช่องทาง: โทรศัพท์ (Call) และ Email (Mail)
- ทำงานวันจันทร์ – ศุกร์

## แผนกที่ให้บริการ

| แผนก | ย่อ | ประเภทงานหลัก |
|---|---|---|
| ASN/EDI | ASN | EDI data, Web Billing, Password reset |
| FAST | FAST | B2P payment, System issues |
| DC | DC | Distribution Center operations |
| GR | GR | Goods Receipt |
| MDS | MDS | Master Data |
| Coface | CF | Credit insurance |
| Vendor | VD | Invoice, Contract |
| Other | OT | งานทั่วไป |

## คำอธิบาย KPI

**FCR (1st Contact Resolution)**
จำนวนสายที่แก้ไขได้ในการโทรครั้งแรก (Level 1) ÷ Call ทั้งหมด
สูงแปลว่าทีมแก้ปัญหาได้เองโดยไม่ต้อง transfer

**FMR (1st Mail Resolution)**
เหมือน FCR แต่สำหรับ Email

**Abandon Rate**
สายที่ลูกค้าวางก่อน agent รับ ÷ สายเข้าทั้งหมด (จาก 3CX)
ยิ่งต่ำยิ่งดี — แปลว่ารอไม่นาน

**Call Reach Rate (SLA)**
สายที่ agent รับได้ ÷ สายเข้า Queue ทั้งหมด (จาก 3CX)
ยิ่งสูงยิ่งดี

**Avg Talk Time**
เวลาเฉลี่ยที่ agent คุยกับลูกค้าต่อสาย (จาก 3CX)

**C2 Transfer (Case Level 2)**
สายที่ต้อง escalate ไปทีมอื่น — ยิ่งต่ำยิ่งดี

**Pending Cases**
Mail ที่ยังไม่ปิด (Status = Pending/Open)
>7 วัน และ >14 วัน ต้องเฝ้าระวังเป็นพิเศษ

## Seasonality

- Call volume สูงในวันจันทร์-อังคาร
- ปลายเดือนมักมี EDI/ASN surge จาก billing cycle
- ช่วง Q1 (ม.ค.-มี.ค.) มักมี volume สูงกว่าปกติ
