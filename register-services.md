#Register services

การดำเนินการต่างๆ ในระบบ จะต้องลงทะเบียนเพื่อเชื่อมต่อ API กับ 3rd party เช่น

##Action

| name |action | api |
|------|--------|-----|-----|
|ยืนยันการสั่งอาหาร|checkoutrestaurant | http://www.mj.com/api/checkout/{userid}/|


##Page

ลงทะเบียน page สำหรับการดึงข้อมูล markdown page จาก 3rd party (ดึงข้อมูลผ่าน API)
- สามารถกำหนด md เริ่มต้นได้

| name |pagename|md |
|------|--------|-----|
|รอการยืนยันสั่งอาหาร      |waitingcheckout       |###Please wait  system in process \![]\(loading.gif\)     |


- หากหน้า page จำเป็นต้องมีการประมวลผลข้อมูลก่อนแสดง สามารถส่งไปให้ api ของ 3rd party ประมวลผลก่อน แล้วส่ง md กลับมาให้ระบบแสดงผล

| name |pagename| api |
|------|--------|-----|
|ยืนยันการสั่งอาหาร |checkoutrestaurant |http://www.mj.com/api/customer/table/{userid}|

##Service
| name |action | api |
|------|--------|-----|-----|
|เรียกพนักงานเสิร์ฟ|callwaiterservice| http://www.mjsuki.com/api/service/callwaiterservice/{userid}/|


