#Register services

การดำเนินการต่างๆ ในระบบ VB จะต้องลงทะเบียนเพื่อเชื่อมต่อ API กับ 3rd party เช่น

##Action

| name |description| action | api |
|------|--------|-----|-----|
|checkoutrestaurant |ยืนยันการสั่งอาหาร| http://www.mj.com/api/checkout/{userid}/|


##Page

ลงทะเบียน page สำหรับการดึงข้อมูล markdown page จาก 3rd party (ดึงข้อมูลผ่าน API)
- สามารถกำหนด md เริ่มต้นได้
- หากหน้า page จำเป็นต้องมีการประมวลผลข้อมูลก่อนแสดง สามารถส่งไปให้ api ของ 3rd party ประมวลผลก่อน แล้วส่ง md กลับมาให้ระบบ VB แสดงผล

| name |description|md | api |
|------|--------|-----|
|checkoutrestaurant |ยืนยันการสั่งอาหาร (ดึงข้อมูลการสั่งจากบริษัทก่อน)| |http://www.mj.com/api/customer/table/{userid}|
|waitingcheckout     |รอการยืนยันสั่งอาหาร        |###Please wait  system in process \![]\(loading.gif\)     ||
