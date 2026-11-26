# ระบบตรวจใบหน้า LIVE · โรงเรียนบ้านนาดอย

หน้าเปิดกล้อง LIVE สำหรับเชื่อมต่อกับระบบบันทึกการมาเรียนของโรงเรียน

- เว็บไซต์: https://patop1241-hub.github.io/school-face-scanner/
- Repository: https://github.com/patop1241-hub/school-face-scanner
- ใช้กล้องผ่าน HTTPS และประมวลผลใบหน้าในเบราว์เซอร์ของเครื่องครู
- รูปอ้างอิงรับมาจากระบบหลักผ่าน postMessage และส่งกลับเฉพาะรหัสนักเรียนที่จับคู่ได้
- วิดีโอจากกล้องไม่ถูกอัปโหลดหรือจัดเก็บโดย GitHub Pages
- ระบบนี้ยังไม่มีการตรวจจับการปลอมแปลงใบหน้า (liveness / anti-spoof) ครูต้องตรวจทานรายชื่อก่อนบันทึก

## การเผยแพร่

ไฟล์ `index.html` อยู่ที่ root ของ branch `main` ส่วน GitHub Actions workflow ที่ `.github/workflows/deploy-pages.yml` จะเผยแพร่เว็บไซต์เมื่อมีการ push ไปยัง `main` หรือเมื่อสั่งรันด้วยตนเอง

## เชื่อมกับเว็บแอปหลัก

ตั้งค่า `ATTENDANCE_FACE_SCANNER_PAGE_URL` ในไฟล์ `Index.html` ของ Apps Script เป็น:

`https://patop1241-hub.github.io/school-face-scanner/`
