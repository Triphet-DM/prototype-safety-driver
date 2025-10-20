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

คำเตือน: สำหรับการติดตั้ง OpenCV อาจต้องใช้วิธีพิเศษที่หลีกเลี่ยงการ Compile จาก Source Code (เช่น การใช้แพ็กเกจที่ Compile สำเร็จรูปผ่าน APT หรือการติดตั้งผ่าน Repository ที่มีการ Optimized ไว้แล้ว)

##  ประสิทธิภาพ (Performance)

* **ฮาร์ดแวร์ที่ใช้ในการทดสอบ:** Raspberry Pi Zero 2 W (32-bit Legacy Lite OS, 0.5 GB RAM)
* **อัตราเฟรมที่ทำได้ (Real-time Test):**
    * เมื่อรันทั้ง 3 ฟังก์ชัน (ตรวจจับใบหน้า, ตรวจจับตา, และ Head Pose) พร้อมกัน โปรเจกต์สามารถทำงานได้ที่ประมาณ **4–7 FPS**