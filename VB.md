#MarkDown Commands
---

##[Consent]

Syntex
    
```
VBConsent[name]("action" "shopid" "nextpage")
```

คำอธิบาย
- ยืนยันการทำรายการของการทำงานต่างๆ

parameter	:
- shopid รหัสร้านค้า
- action แอคชั่นที่ต้องการยืนยัน เช่น ยืนยันการสั่งอาหาร , ยืนยันการโอนจ่าย etc. (action ที่สามารถสั่งได้ ต้องทำการ ลงทะเบียนก่อน)
- nextpage หน้าถัดไปที่ต้องการไปต่อ (page ที่ใช้ต้องทำการลงทะเบียนก่อน)


Example Code
```
VBConsent[ยืนยันจ่ายเงิน]("restaurant" "mk" "mklandpage")
```

Example UI

![](/assets/consent.jpg)

##[AddItems]
คำอธิบาย
- เพิ่มสินค้าลงตะกร้า

parameter :
- shopid รหัสร้านค้า
- Item รายละเอียดสินค้า
- action example : individual (เพิ่มสินค้าลงตะกร้าทันที) , bypass ( ยังไม่เพิ่มทันที 3rd party จะ เพิ่มสินค้าลงตะกร้าเองภายหลัง)
- nextpage หน้าถัดไปที่ต้องการไปต่อ (page ที่ใช้ต้องทำการลงทะเบียนก่อน)

Example Code
- [AddItems(action="checkout")]

Example UI

##[EditItemDetail]   
คำอธิบาย
- แก้ไขรายละเอียดสินค้า

parameter :
- shopid รหัสร้านค้า
- oldid รหัสสินค้าที่ต้องการแก้ไข
- Items รายละเอียดสินค้าใหม่
- nextpage หน้าถัดไปที่ต้องการไปต่อ (page ที่ใช้ต้องทำการลงทะเบียนก่อน)

Example Code

Example UI

##[GoToCheckOut(action="checkout")] 	

Syntex
    
```
VBGotoCheckOut[name]()
```


คำอธิบาย
- เปลี่ยนไปหน้าตะกร้าสินค้า

no parameter

Example Code

Example UI

##[SubmitForm] 	
คำอธิบาย
- ข้อมูลที่ต้องการจาก ผู้ใช้งาน โดยสามารถรับข้อมูลได้เฉพาะที่เว็บกำหนด
* ชื่อ
* ที่อยู่
* เบอโทรศัพท์

parameter :
- shopid รหัสร้านค้า
- InputsFroms
- action
- nextpage หน้าถัดไปที่ต้องการไปต่อ (page ที่ใช้ต้องทำการลงทะเบียนก่อน)

Example Code

Example UI

##[CallService] 

Syntex
```
VBCallService[name]("servicename")
```
คำอธิบาย
- เรียก service

parameter :
- servicename ชื่อ service ที่ต้องการเรียก (service ที่ใช้ต้องทำการลงทะเบียนก่อน)

Example Code

Example UI

##[CallPage] 

Syntex
```
VBCallPage[name]("pagename")
```

คำอธิบาย
- เปลี่ยนหน้า

parameter :
- pagename หน้าถัดไปที่ต้องการไปต่อ (page ที่ใช้ต้องทำการลงทะเบียนก่อน)

Example Code

Example UI