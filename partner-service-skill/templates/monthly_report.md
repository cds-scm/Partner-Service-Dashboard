# Template: Monthly Report

รายงานประจำเดือนสำหรับผู้บริหารและทีมงาน เน้นครบถ้วน มีข้อมูลเชิงลึก

## จำนวน Slides: 7-8 slides

### Slide ที่ต้องมี (ตามลำดับ)

1. **cover** — ชื่อรายงาน + เดือน/ปี + แผนก
2. **kpi_overview** — KPI หลัก 5 ตัว (FCR, FMR, Abandon, Reach Rate, Avg Talk)
3. **fcr_detail** — FCR แยกตามแผนก + trend เปรียบเทียบเดือนก่อน
4. **dept_summary** — สรุปรายแผนก (Call/Mail/Pending แต่ละแผนก)
5. **top_issues** — Top 5 ปัญหาที่พบบ่อย + จำนวน
6. **pending_cases** — Case ค้าง แยก >7วัน, >14วัน + แผนกที่ค้างมาก
7. **strengths_concerns** — จุดแข็ง vs จุดปรับปรุง (2 คอลัมน์)
8. **recommendation** — Action items พร้อม owner + timeline

### Design Style

```
สี header bar   : #1E1B3A (ดำเข้ม)
สี accent       : #FCD34D (เหลือง)
สี primary      : #6C5CE7 (ม่วง)
สี background   : #FFFFFF
font header     : CPN Bold 28px
font body       : CPN Regular 14px
```

### Narrative Tone

- ทางการปานกลาง เหมาะสำหรับ meeting
- ระบุตัวเลขเปรียบเทียบกับเดือนก่อนทุกครั้ง
- สรุปประเด็นสำคัญไม่เกิน 3 ข้อต่อ slide

### KPI Grid Layout (slide kpi_overview)

แสดง KPI เป็น 5 การ์ด แถวเดียว แต่ละการ์ดมี:
- ค่า KPI ใหญ่ตรงกลาง
- label ด้านล่าง
- trend (เปรียบเทียบเดือนก่อน) มุมขวาบน สีเขียว/แดง
- สีขอบการ์ดตาม status (green/amber/red)

### FCR Detail Slide

- Bar chart แนวนอน แยกรายแผนก
- แต่ละ bar แสดง FCR% + จำนวน (n/total)
- เส้นแนวตั้งแสดงเป้าหมาย 85%
- แผนกที่ต่ำกว่าเป้าแสดง bar สีแดง

### Pending Cases Slide

แสดง 4 metric boxes:
- Total pending, >7 วัน, >14 วัน, Avg pending time
และตาราง top แผนกที่มี case ค้างมากสุด
