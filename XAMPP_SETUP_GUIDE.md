# 🚀 دليل إعداد XAMPP للمشروع

## 📁 **المسار المطلوب بالضبط**
```
C:\xampp\htdocs\project\backend\
```

## ✅ **خطوات الإعداد السريع**

### 1️⃣ **تشغيل XAMPP**
```bash
# افتح XAMPP Control Panel
# انقر على "Start" بجانب Apache
# تأكد أن الحالة أصبحت "Running" (أخضر)
```

### 2️⃣ **نسخ ملفات الباك إند**
```bash
# انسخ هذه الملفات إلى:
C:\xampp\htdocs\project\backend\process.php
C:\xampp\htdocs\project\backend\puppeteer_cart_search.js
C:\xampp\htdocs\project\backend\README.md
```

### 3️⃣ **اختبار الاتصال**
```bash
# افتح المتصفح واذهب إلى:
http://localhost/project/backend/process.php

# يجب أن تظهر رسالة خطأ (هذا طبيعي)
# إذا ظهرت صفحة 404، فالمسار خاطئ
```

## 🔧 **استكشاف الأخطاء**

### ❌ **Apache لا يعمل**
```bash
🔧 الحلول:
1. تأكد من إغلاق Skype (يستخدم المنفذ 80)
2. تأكد من عدم تشغيل IIS
3. غير المنفذ إلى 8080 إذا لزم الأمر
4. أعد تشغيل XAMPP كمدير
```

### ❌ **404 Not Found**
```bash
🔧 الحلول:
1. تأكد من المسار: C:\xampp\htdocs\project\backend\
2. تأكد من وجود ملف process.php
3. تأكد من تشغيل Apache
4. جرب: http://127.0.0.1/project/backend/process.php
```

### ❌ **500 Internal Server Error**
```bash
🔧 الحلول:
1. تحقق من ملف: C:\xampp\apache\logs\error.log
2. تأكد من صحة ملف process.php
3. تأكد من إصدار PHP (7.4+)
4. تحقق من صلاحيات الملفات
```

### ❌ **Access Denied**
```bash
🔧 الحلول:
1. شغل XAMPP كمدير (Run as Administrator)
2. تحقق من صلاحيات المجلد
3. تأكد من إعدادات Firewall
4. تحقق من إعدادات Antivirus
```

## 🎯 **اختبارات التحقق**

### ✅ **اختبار 1: Apache يعمل**
```bash
# اذهب إلى: http://localhost
# يجب أن تظهر صفحة XAMPP الرئيسية
```

### ✅ **اختبار 2: PHP يعمل**
```bash
# أنشئ ملف test.php في C:\xampp\htdocs\
# اكتب فيه: <?php phpinfo(); ?>
# اذهب إلى: http://localhost/test.php
```

### ✅ **اختبار 3: المسار صحيح**
```bash
# اذهب إلى: http://localhost/project/backend/process.php
# يجب أن تظهر رسالة خطأ (ليس 404)
```

### ✅ **اختبار 4: الملفات موجودة**
```bash
# تحقق من وجود:
C:\xampp\htdocs\project\backend\process.php ✓
C:\xampp\htdocs\project\backend\puppeteer_cart_search.js ✓
```

## 🚀 **بعد الإعداد**

### 1️⃣ **تشغيل المشروع**
```bash
npm start
```

### 2️⃣ **اختبار التحليل**
```bash
# استخدم أي رابط من القائمة الجديدة
# مثال: https://olympus-eshop.com/en/product-category/accessories/
```

### 3️⃣ **مراقبة السجلات**
```bash
# افتح الترمينال في المشروع
# راقب الرسائل المباشرة أثناء التحليل
```

## 📞 **الدعم السريع**

### 🔍 **إذا لم يعمل:**
1. تأكد من تشغيل Apache (أخضر في XAMPP)
2. تأكد من المسار: `C:\xampp\htdocs\project\backend\`
3. اختبر: `http://localhost/project/backend/process.php`
4. راجع ملف: `C:\xampp\apache\logs\error.log`

### ✅ **علامات النجاح:**
- Apache يعمل (أخضر)
- الرابط يعطي خطأ (ليس 404)
- الملفات في المسار الصحيح
- المشروع يتصل بالباك إند

---

**🎉 بعد اتباع هذه الخطوات، المشروع سيعمل بشكل مثالي مع XAMPP!**