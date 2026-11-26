# ระบบตรวจใบหน้า LIVE · โรงเรียนบ้านนาดอย

หน้าเปิดกล้อง LIVE สำหรับเชื่อมต่อกับระบบบันทึกการมาเรียนของโรงเรียน

- เว็บไซต์: https://patop1241-hub.github.io/school-face-scanner/
- Repository: https://github.com/patop1241-hub/school-face-scanner
- ใช้กล้องผ่าน HTTPS และประมวลผลใบหน้าในเบราว์เซอร์ของเครื่องครู
- รูปอ้างอิงรับมาจากระบบหลักผ่าน postMessage และส่งกลับเฉพาะรหัสนักเรียนที่จับคู่ได้
- วิดีโอจากกล้องไม่ถูกอัปโหลดหรือจัดเก็บโดย GitHub Pages
- ระบบนี้ยังไม่มีการตรวจจับการปลอมแปลงใบหน้า (liveness / anti-spoof) ครูต้องตรวจทานรายชื่อก่อนบันทึก

## เปิดใช้ GitHub Pages ครั้งแรก

ไปที่ Settings > Pages ของ Repository นี้ แล้วตั้งค่า Build and deployment > Source เป็น **GitHub Actions** จากนั้น Save หากมีปุ่มแสดง ขั้นตอนนี้จำเป็นครั้งเดียว เพราะ GitHub Actions ที่เชื่อมต่ออยู่ไม่มีสิทธิ์เปิด Pages site ครั้งแรกแทนเจ้าของ Repository ได้

หลังเปิด Pages แล้ว ให้รัน workflow **Deploy face scanner to GitHub Pages** จากแท็บ Actions หรือแจ้งผู้ช่วยเพื่อสั่งรันและตรวจสอบให้

## เชื่อมกับเว็บแอปหลัก

ตั้งค่า `ATTENDANCE_FACE_SCANNER_PAGE_URL` ในไฟล์ `Index.html` ของ Apps Script เป็น:

`https://patop1241-hub.github.io/school-face-scanner/`
