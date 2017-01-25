# vb-client-api-doc

Virtual Bank Client API Docuemntation



\#\#  Consent

&gt; GET   api/consent/{shopid}/{action}/{pagename}

        ใช้เมื่อต้องการให้ user ยินยอมข้อตกลงที่ต้องการ



        \[action\]        กำหนดการทำงานของข้อตกลง

            - transfer    สำหรับการโอนจ่ายเงิน

            - restaurant  สำหรับยืนยันการเช็คอินโต๊ะของร้านอาหาร



\#\# Shopping 



POST    api/AddItems/   

POST    api/EditItem/

         api/RemoveItem/{shopid}/{itemid}/{pagename}



\#\# Form



GET    api/autofill/{password}/{page}

POST   api/SubmitForm/                         shopid, Inputs, action, nextpage



\#\# Navigate & utilities \( Page , Service \) before



GET     api/callservice/{servicename}

    api/getpage/{pagename}





AddItemsRequest Sample

{

    "shopid":"1",

    "action":"individual",

    "nextpage":"",

    "items" :\[  

        { 

            "id":"332131",

            "quantity":2

        },

        { 

            "id":"321321",

            "quantity":1

        },

    \],

}



EditItemsRequest Sample

{

    "shopid":"1",

    "OldItemid":"11321",

    "nextpage":"",

    "item" :\[  

        { 

            "id":"332131",

            "quantity":2

        }       

    \],

}

