#MarkDown Commands
---

##[Consent]

Syntax
    
```
$[Consent]("title": "action" "shopid" "nextpage")
```

คำอธิบาย
- ยืนยันการทำรายการของการทำงานต่างๆ

parameter	:
- shopid รหัสร้านค้า
- action แอคชั่นที่ต้องการยืนยัน เช่น ยืนยันการสั่งอาหาร , ยืนยันการโอนจ่าย etc. (action ที่สามารถสั่งได้ ต้องทำการ ลงทะเบียนก่อน)
- nextpage หน้าถัดไปที่ต้องการไปต่อ (page ที่ใช้ต้องทำการลงทะเบียนก่อน #ไม่ใส่หากหน้าต่อไปต้องการกลับไประบบ VB)


Example Code
```
$[Consent]("ยืนยัน": "checkoutrestaurant" "mk" "")
```

Example UI

![](/assets/consent.jpg)

##[AddItems]

Syntax
    
```
$[AddItem]("title": "action" "productid" "shopid" "nextpage")
```


คำอธิบาย
- เพิ่มสินค้าลงตะกร้า

parameter :
- shopid รหัสร้านค้า
- Item รายละเอียดสินค้า
- action example : 
    - individual (เพิ่มสินค้าลงตะกร้าทันที) 
    - bypass ( ยังไม่เพิ่มทันที แต่จะส่งข้อมูลให้ 3rd party ก่อน และ 3rd party จะเพิ่มสินค้าลงตะกร้าเองภายหลัง)
- nextpage หน้าถัดไปที่ต้องการไปต่อ (page ที่ใช้ต้องทำการลงทะเบียนก่อน #ไม่ใส่หากหน้าต่อไปต้องการกลับไประบบ VB)

Example Code
```
$[AddItem]("เพิ่มสินค้า": "individual" "nmd01bls30" "adidas" "")
```

Example UI

##[EditItemDetail]   

Syntax
    
```
$[EditItem]("title": "shopid" "oldproductid" "newproductid" "nextpage")
```

คำอธิบาย
- แก้ไขรายละเอียดสินค้า

parameter :
- shopid รหัสร้านค้า
- oldproductid รหัสสินค้าที่ต้องการแก้ไข
- newproductid รายละเอียดสินค้าใหม่
- nextpage หน้าถัดไปที่ต้องการไปต่อ (page ที่ใช้ต้องทำการลงทะเบียนก่อน #ไม่ใส่หากหน้าต่อไปต้องการกลับไประบบ VB)

Example Code

```
$[EditItem]("แก้ไข": "adidas" "nmd01bls30" "nmd01whs30" "")
```

Example UI

##[GoToCheckOut] 	

Syntax
    
```
$[GotoCheckOut]("name")
```


คำอธิบาย
- navigate เปลี่ยนไปหน้าตะกร้าสินค้าของระบบ

no parameter

Example Code
```
$[GotoCheckOut]("เปิดตะกร้า")
```


Example UI

##[SubmitForm] 	

Syntax
```
$[SubmitForm]("title": "action")
    ?{shopid}("shopid" "value"){.form-control}
    ?{nextpage}("nextpage" "value"){.form-control}
    
    ?{type}("label" "value" "placeholder" rows*cols){.class}
    .
    ..
    ...
    ?{submit}("" "Send!"){.form-control}
[/SubmitForm]
```

คำอธิบาย
- ข้อมูลที่ต้องการจาก ผู้ใช้งาน โดยสามารถรับข้อมูลได้เฉพาะที่เว็บกำหนด
* ชื่อ
* ที่อยู่
* เบอโทรศัพท์

parameter :
- shopid รหัสร้านค้า
- InputsFroms ข้อมูลต่างๆที่ต้องการจาก user
- action
- nextpage หน้าถัดไปที่ต้องการไปต่อ (page ที่ใช้ต้องทำการลงทะเบียนก่อน #ไม่ใส่หากหน้าต่อไปต้องการกลับไประบบ VB)

Example Code
```
$[SubmitForm]("topupgame": "")
    ?{shopid}("shopid" "ragnarok"){.form-control}
    ?{nextpage}("nextpage" "gamemenu"){.form-control}
    
    ?{text}("UserCode" "" "" ){.form-control}
    
    ?{submit}("" "ขั้นตอนต่อไป"){.form-control}
$[/SubmitForm]
```



Example UI

##[CallService] 

Syntax
```
$[CallService]("title": "shopid" "servicename")
```
คำอธิบาย
- เรียก service

parameter :
- shopid รหัสร้านค้า
- servicename ชื่อ service ที่ต้องการเรียก (service ที่ใช้ต้องทำการลงทะเบียนก่อน)

Example Code
```
$[CallService]("CallWaiter": "mjsuki" "callwaiterservice")
```

Example UI

##[CallPage] 

Syntax
```
&[CallPage]("title": "shopid" "pagename")
```

คำอธิบาย
- เปลี่ยนหน้า

parameter :
- shopid รหัสร้านค้า
- pagename หน้าถัดไปที่ต้องการไปต่อ (page ที่ใช้ต้องทำการลงทะเบียนก่อน)

Example Code
```
&[CallPage]("homemenu": "niki" "landpage")
```

Example UI