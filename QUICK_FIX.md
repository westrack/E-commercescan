# ⚡ إصلاح سريع - 5 دقائق

## 🎯 **اتبع هذه الخطوات بالترتيب**

### 1️⃣ **تشغيل XAMPP (30 ثانية)**
```bash
# افتح XAMPP Control Panel
# انقر "Start" بجانب Apache
# انتظر حتى يصبح أخضر
```

### 2️⃣ **اختبار Apache (30 ثانية)**
```bash
# افتح المتصفح
# اذهب إلى: http://localhost
# يجب أن تظهر صفحة XAMPP
```

### 3️⃣ **إنشاء المجلدات (1 دقيقة)**
```bash
# افتح File Explorer
# اذهب إلى: C:\xampp\htdocs\
# أنشئ مجلد: project
# داخل project أنشئ مجلد: backend
```

### 4️⃣ **نسخ الملفات (2 دقيقة)**
```bash
# من مجلد المشروع الحالي:
# انسخ backend/process.php
# الصق في: C:\xampp\htdocs\project\backend\

# انسخ backend/puppeteer_cart_search.js  
# الصق في: C:\xampp\htdocs\project\backend\
```

### 5️⃣ **اختبار الاتصال (30 ثانية)**
```bash
# افتح المتصفح
# اذهب إلى: http://localhost/project/backend/process.php
# يجب أن تظهر رسالة خطأ (ليس 404)
```

### 6️⃣ **تشغيل المشروع (30 ثانية)**
```bash
# في terminal المشروع:
npm start
```

## ✅ **علامات النجاح**
- Apache أخضر في XAMPP ✓
- http://localhost يعمل ✓  
- الملفات في المسار الصحيح ✓
- المشروع يتصل بالباك إند ✓

## ❌ **إذا لم يعمل**
أرسل لي:
1. لون Apache في XAMPP (أخضر/أحمر)
2. ما يظهر عند فتح http://localhost
3. ما يظهر عند فتح http://localhost/project/backend/process.php

**سأحل المشكلة فوراً!** 🚀