# 🔧 دليل حل مشاكل XAMPP - خطوة بخطوة

## 🚨 **المشكلة الحالية**
```
❌ لا يمكن الاتصال بخادم الباك إند
```

## ✅ **الحلول المرتبة حسب الأولوية**

### 🔥 **الحل الأول: التحقق من XAMPP**

#### 1️⃣ **افتح XAMPP Control Panel**
```bash
# اذهب إلى: C:\xampp\xampp-control.exe
# أو ابحث عن "XAMPP" في قائمة Start
```

#### 2️⃣ **تشغيل Apache**
```bash
# انقر على "Start" بجانب Apache
# يجب أن يصبح اللون أخضر ويظهر "Running"
# إذا لم يعمل، انظر للحلول أدناه
```

#### 3️⃣ **اختبار Apache**
```bash
# افتح المتصفح واذهب إلى:
http://localhost

# يجب أن تظهر صفحة XAMPP الرئيسية
# إذا لم تظهر، Apache لا يعمل
```

### 🔥 **الحل الثاني: نسخ الملفات بالطريقة الصحيحة**

#### 1️⃣ **إنشاء المجلدات**
```bash
# أنشئ هذا المسار إذا لم يكن موجوداً:
C:\xampp\htdocs\project\
C:\xampp\htdocs\project\backend\
```

#### 2️⃣ **نسخ الملفات**
```bash
# انسخ من مجلد المشروع:
من: C:\xampp\htdocs\project\backend\process.php
إلى: C:\xampp\htdocs\project\backend\process.php

من: C:\xampp\htdocs\project\backend\puppeteer_cart_search.js  
إلى: C:\xampp\htdocs\project\backend\puppeteer_cart_search.js
```

#### 3️⃣ **التحقق من الملفات**
```bash
# تأكد من وجود:
C:\xampp\htdocs\project\backend\process.php ✓
C:\xampp\htdocs\project\backend\puppeteer_cart_search.js ✓
```

### 🔥 **الحل الثالث: اختبار الاتصال**

#### 1️⃣ **اختبار مباشر**
```bash
# افتح المتصفح واذهب إلى:
http://localhost/project/backend/process.php

# النتائج المتوقعة:
✅ رسالة خطأ PHP (طبيعي) = يعمل
❌ 404 Not Found = المسار خاطئ
❌ لا يمكن الوصول = Apache لا يعمل
```

#### 2️⃣ **اختبار بديل**
```bash
# جرب أيضاً:
http://127.0.0.1/project/backend/process.php
http://localhost:80/project/backend/process.php
```

## 🚨 **حلول المشاكل الشائعة**

### ❌ **Apache لا يبدأ**

#### السبب: المنفذ 80 مستخدم
```bash
🔧 الحل:
1. أغلق Skype تماماً
2. أوقف IIS إذا كان يعمل
3. أعد تشغيل XAMPP كمدير (Run as Administrator)
```

#### السبب: Firewall أو Antivirus
```bash
🔧 الحل:
1. أضف XAMPP لاستثناءات Firewall
2. أضف مجلد C:\xampp لاستثناءات Antivirus
3. أعد تشغيل الكمبيوتر
```

### ❌ **404 Not Found**

#### السبب: المسار خاطئ
```bash
🔧 الحل:
1. تأكد من المسار: C:\xampp\htdocs\project\backend\
2. تأكد من وجود ملف process.php
3. تأكد من كتابة الرابط صحيح
```

### ❌ **500 Internal Server Error**

#### السبب: خطأ في ملف PHP
```bash
🔧 الحل:
1. راجع ملف: C:\xampp\apache\logs\error.log
2. تأكد من صحة ملف process.php
3. تأكد من إصدار PHP (7.4+)
```

### ❌ **Access Denied**

#### السبب: صلاحيات
```bash
🔧 الحل:
1. شغل XAMPP كمدير
2. غير صلاحيات المجلد C:\xampp\htdocs\project\
3. تأكد من عدم حماية المجلد
```

## 🎯 **خطوات التحقق النهائية**

### ✅ **قائمة التحقق**
```bash
□ XAMPP Control Panel مفتوح
□ Apache يعمل (أخضر)
□ http://localhost يعمل
□ الملفات في C:\xampp\htdocs\project\backend\
□ http://localhost/project/backend/process.php يعطي خطأ (ليس 404)
```

### ✅ **اختبار نهائي**
```bash
# إذا كل شيء يعمل:
1. شغل المشروع: npm start
2. جرب تحليل أي رابط
3. راقب الترمينال للرسائل
```

## 🆘 **إذا لم يعمل أي شيء**

### 🔄 **إعادة تثبيت XAMPP**
```bash
1. احذف XAMPP تماماً
2. حمل أحدث إصدار من: https://www.apachefriends.org/
3. ثبت في C:\xampp\
4. شغل كمدير
5. اتبع الخطوات من البداية
```

### 🔄 **استخدام منفذ بديل**
```bash
# في XAMPP Control Panel:
1. انقر "Config" بجانب Apache
2. اختر "httpd.conf"
3. غير "Listen 80" إلى "Listen 8080"
4. احفظ وأعد تشغيل Apache
5. استخدم: http://localhost:8080/project/backend/process.php
```

---

## 📞 **دعم سريع**

### 🔍 **للتشخيص السريع:**
1. ما هي رسالة الخطأ عند فتح http://localhost ؟
2. هل Apache أخضر في XAMPP Control Panel؟
3. هل الملفات موجودة في C:\xampp\htdocs\project\backend\ ؟
4. ما هي رسالة الخطأ عند فتح http://localhost/project/backend/process.php ؟

**أرسل إجابات هذه الأسئلة وسأساعدك فوراً!** 🚀