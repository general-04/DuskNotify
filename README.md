# DarkAlert 🌑

<div align="center">
  
![DarkAlert Banner](https://raw.githubusercontent.com/general-04/DarkAlert/refs/heads/main/LogoDarkAlertv2.jpg)

**DuskNotify9Level**

[![Version](https://img.shields.io/badge/version-2.0.0-8B5CF6.svg)](https://github.com/general-04/DuskNotify)
[![Size](https://img.shields.io/badge/size-60kb-4F46E5.svg)]()

</div>

## ✨ คุณสมบัติ

- 🌑 ธีมดาร์กโหมดที่ออกแบบมาแบบเดียว
- 📱 Responsive Design
- 🛠️ Flexible customization  

## 📦 การติดตั้ง

### วิธีที่ 1: ผ่าน CDN

```html
<link href="https://cdn.jsdelivr.net/gh/general-04/DarkAlert@main/DuskNotify.min.css" rel="stylesheet">
<script src="https://cdn.jsdelivr.net/gh/general-04/DarkAlert@main/DuskNotify.min.js"></script>
```

### วิธีที่ 2: ดาวน์โหลด

[ดาวน์โหลด DuskNotify v2.2.0](https://github.com/general-04/DuskNotify/)

## 🚀 การใช้งานเบื้องต้น

```javascript
// แจ้งเตือนพื้นฐาน
Dusk.fire({
    title: 'การแจ้งเตือนพื้นฐาน',
    text: 'สวัสดี!'
});

// แจ้งเตือนสำเร็จ
Dusk.success({
    title: 'สำเร็จ!',
    text: 'ดำเนินการเสร็จสิ้น'
});

// แจ้งเตือนผิดพลาด
Dusk.error({
    title: 'ผิดพลาด!',
    text: 'เกิดข้อผิดพลาดบางอย่าง'
});

// Toast การแจ้งเตือน
Dusk.successToast({
    text: 'บันทึกข้อมูลเรียบร้อย'
});
```

## ⚙️ การกำหนดค่า

```javascript
Dusk.fire({
    title: '',                 // หัวข้อ
    text: '',                  // ข้อความ
    icon: 'info',              // ไอคอน (info, success, error, warning, loading)
    showConfirmButton: true,   // แสดงปุ่มยืนยัน
    showCancelButton: false,   // แสดงปุ่มยกเลิก
    confirmButtonText: 'OK',   // ข้อความปุ่มยืนยัน
    cancelButtonText: 'Cancel',// ข้อความปุ่มยกเลิก
    confirmCallback: null,     // ฟังก์ชันเมื่อคลิกปุ่มยืนยัน
    cancelCallback: null,      // ฟังก์ชันเมื่อคลิกปุ่มยกเลิก
    closeOnOverlayClick: true, // ปิดเมื่อคลิกภายนอก
    progress: false,           // แสดงแถบโหลด
    timer: null,               // ตั้งเวลาปิดอัตโนมัติ (มิลลิวินาที)
    position: 'center',        // ตำแหน่ง (center, top, bottom)
    animation: true,           // เปิด/ปิดการเคลื่อนไหว
    customClass: '',           // คลาสเพิ่มเติม
    allowOutsideClick: true,   // อนุญาตให้คลิกภายนอกเพื่อปิด
    backdrop: true,            // แสดงพื้นหลังทึบ
    toast: false,              // โหมด Toast
    toastPosition: 'bottom-end'// ตำแหน่ง Toast
});
```

## 🎭 ประเภทการแจ้งเตือน

Dusk มาพร้อมกับประเภทการแจ้งเตือนสำเร็จรูปหลายแบบ:

### การแจ้งเตือนพื้นฐาน

```javascript
Dusk.fire({
    title: 'การแจ้งเตือนพื้นฐาน',
    text: 'สวัสดี!'
});
```

### การแจ้งเตือนสำเร็จ

```javascript
Dusk.success({
    title: 'สำเร็จ!',
    text: 'ดำเนินการเสร็จสิ้น'
});
```

### การแจ้งเตือนข้อผิดพลาด

```javascript
Dusk.error({
    title: 'ผิดพลาด!',
    text: 'เกิดข้อผิดพลาดบางอย่าง'
});
```

### การแจ้งเตือนคำเตือน

```javascript
Dusk.warning({
    title: 'คำเตือน!',
    text: 'โปรดระมัดระวัง'
});
```

### การแจ้งเตือนข้อมูล

```javascript
Dusk.info({
    title: 'ข้อมูล',
    text: 'นี่คือข้อมูลสำคัญ'
});
```

## 🍞 การใช้งานโหมด Toast

Toast เป็นการแจ้งเตือนแบบชั่วคราวที่ปรากฏที่มุมหน้าจอ:

```javascript
// Toast สำเร็จ
Dusk.successToast({
    text: 'บันทึกข้อมูลเรียบร้อย'
});

// Toast ผิดพลาด
Dusk.errorToast({
    text: 'ไม่สามารถบันทึกข้อมูลได้'
});

// Toast คำเตือน
Dusk.warningToast({
    text: 'การเชื่อมต่อไม่เสถียร'
});

// กำหนดตำแหน่ง Toast
Dusk.successToast({
    text: 'บันทึกข้อมูลเรียบร้อย',
    toastPosition: 'top-end' // top, top-start, top-end, bottom, bottom-start, bottom-end
});
```

## 🔥 เริ่มโหด

### การยืนยันการทำรายการ

```javascript
Dusk.fire({
    title: 'ยืนยันการทำรายการ',
    text: 'คุณต้องการดำเนินการต่อหรือไม่?',
    showCancelButton: true,
    confirmButtonText: 'ยืนยัน',
    cancelButtonText: 'ยกเลิก',
    confirmCallback: () => {
        console.log('ผู้ใช้ยืนยันการทำรายการ');
    },
    cancelCallback: () => {
        console.log('ผู้ใช้ยกเลิกการทำรายการ');
    }
});
```

### การปิดอัตโนมัติ

```javascript
Dusk.fire({
    title: 'ปิดอัตโนมัติ',
    text: 'จะปิดใน 2 วินาที',
    timer: 2000
});
```

### สถานะกำลังโหลด

```javascript
Dusk.loading({
    title: 'กำลังโหลด',
    text: 'กรุณารอสักครู่...'
});

// ปิดการแจ้งเตือนกำลังโหลด
setTimeout(() => {
    Dusk.close();
}, 3000);
```
