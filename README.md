# PetTracks

เว็บแอปสำหรับจัดการข้อมูลสัตว์เลี้ยงและติดตามตำแหน่งจากมือถือ
พร้อมแสดงพิกัดบนแผนที่และแจ้งเตือนเมื่อออกนอกพื้นที่ปลอดภัย

## Features
- สมัครสมาชิกและเข้าสู่ระบบด้วย JWT พร้อมแฮชรหัสผ่านด้วย bcrypt
- เพิ่ม แก้ไข ลบข้อมูลสัตว์เลี้ยง และอัปโหลดรูปภาพ
- รับพิกัดจากมือถือผ่าน Geolocation API และส่งไปยัง Flask ผ่าน ngrok
- แสดงตำแหน่งด้วย Leaflet และ OpenStreetMap โดยดึงข้อมูลทุก 5 วินาที
- กำหนดพื้นที่ปลอดภัยและแจ้งเตือนบนหน้าเว็บเมื่อพิกัดอยู่นอกพื้นที่

## Tech Stack
- Frontend: Vue.js, Tailwind CSS, Leaflet
- Backend: Node.js, Express.js, Python, Flask
- Database: PostgreSQL
- Deployment: Docker Compose, Jenkins, Google Cloud Platform
- Mobile Access: ngrok

## Implementation
ใช้ Docker Compose จัดการบริการ และ Jenkins สำหรับสร้าง Docker images
และเริ่ม containers โดยมีการนำระบบขึ้นใช้งานบน GCP

ปัจจุบันระบบแสดงพิกัดล่าสุดจากส่วนกลาง ยังไม่ผูกพิกัดแยกตามสัตว์แต่ละตัว
