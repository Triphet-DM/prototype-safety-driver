# Prototype Safety Driver (ระบบตรวจจับความปลอดภัยเบื้องต้น)

โปรเจกต์นี้มีจุดมุ่งหมายเพื่อทดสอบการตรวจจับองค์ประกอบใบหน้า (Face, Eyes, Head Pose) แบบ Real-time บนฮาร์ดแวร์จำกัด เช่น Raspberry Pi Zero 2 W

---

## ⚙️ Dependencies (สิ่งที่จำเป็นต้องติดตั้ง)

โปรเจกต์นี้ใช้ Library ที่ระบุในไฟล์ `requirements.txt`

### หมายเหตุสำคัญสำหรับผู้ใช้ Raspberry Pi Zero 2 W

เนื่องจากข้อจำกัดด้าน RAM (0.5 GB) ของบอร์ด Raspberry Pi Zero 2 W (32-bit Legacy OS) **การติดตั้ง `opencv-python` โดยตรงด้วย `pip` มักจะล้มเหลว** หรือใช้เวลานานมาก

* **วิธีการติดตั้ง Library ที่แนะนำ:** หลังโคลนโปรเจกต์ไปแล้ว ให้รันคำสั่งติดตั้ง Dependencies บน Raspberry Pi:
  ```bash
  pip install -r requirements.txt