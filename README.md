# 📦 ระบบติดตามพัสดุ (Parcel Dashboard)

Dashboard สำหรับติดตามพัสดุแบบ Real-time จาก Google Sheets  
แสดงข้อมูลเฉพาะสถานะ **"นำเข้า"** เท่านั้น

## 🌐 เปิดใช้งาน

👉 **[คลิกเพื่อเปิด Dashboard](https://YOUR-USERNAME.github.io/YOUR-REPO-NAME)**

---

## ⚙️ วิธีตั้งค่า

### 1. Fork หรือ Upload ไฟล์นี้ไปยัง GitHub Repository

### 2. เปิด GitHub Pages
1. ไปที่ **Settings** → **Pages**
2. Source: เลือก **Deploy from a branch**
3. Branch: เลือก **main** → folder **/ (root)**
4. กด **Save**
5. รอประมาณ 1-2 นาที จะได้ URL สาธารณะ

### 3. ตั้งค่า Google Sheets
1. เปิด Google Sheets ที่ต้องการ
2. กด **แชร์** (Share) มุมขวาบน
3. เปลี่ยนเป็น **"Anyone with the link can view"**
4. คัดลอก **Spreadsheet ID** จาก URL:
   ```
   https://docs.google.com/spreadsheets/d/[SPREADSHEET_ID]/edit
   ```
5. ใส่ Spreadsheet ID ในหน้า Dashboard แล้วกด **"เชื่อมต่อ Sheet"**

---

## 📋 โครงสร้างคอลัมน์ใน Google Sheets

| คอลัมน์ | ข้อมูล |
|---------|--------|
| A | วันที่ |
| B | เลขพัสดุ |
| C | บริษัทขนส่ง |
| D | สถานะ (ต้องเป็น "นำเข้า") |
| E | ดำเนินการ |
| F | ชั้นวาง |
| G | วันหมดอายุ |
| H | รูปภาพ (path) |
| L | image link (Google Drive URL) |
| M | สาเหตุปัญหา |

> ⚠️ **หมายเหตุ:** Dashboard จะดึงเฉพาะแถวที่มี **วันที่** และ **สถานะ = "นำเข้า"** เท่านั้น

---

## ✨ ฟีเจอร์

- 📊 **Stats Cards** — นำเข้าวันนี้, สัปดาห์, เดือน, ใกล้หมดอายุ, มีปัญหา
- 🔍 **ค้นหา** — ค้นหาเลขพัสดุแบบ real-time
- 🗓️ **กรองตามช่วงเวลา** — วันนี้ / สัปดาห์ / เดือน / กำหนดเอง
- 🏢 **กรองตามบริษัท** — Lazada, Flash, J&T, Shopee, Kerry ฯลฯ
- ⚠️ **กรองตามสาเหตุ** — กระดาษเลือนลาง, ไม่ระบุสาขา ฯลฯ
- 📷 **ดูรูปภาพ** — คลิกเพื่อดูรายละเอียดและรูปพัสดุ
- 📈 **กราฟ** — แนวโน้ม 7 วัน, บริษัทขนส่ง, สาเหตุปัญหา
- ⬇️ **Export CSV** — ส่งออกข้อมูลที่กรองแล้ว
- 🔄 **Auto Refresh** — อัปเดตอัตโนมัติทุก 5 นาที

---

## 🛠️ เทคโนโลยี

- HTML / CSS / JavaScript (ไม่มี dependency พิเศษ)
- Google Sheets GViz API (ดึงข้อมูลแบบ Public)
- Google Fonts (Sarabun, IBM Plex Mono)
- Deploy บน GitHub Pages (ฟรี)
