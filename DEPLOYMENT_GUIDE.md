# دليل نشر موقع ثانوية 2026
## تصميم: محمد العوضي شاهين

---

## الخطوات — من الصفر للنشر على Google في 30 دقيقة

---

### الخطوة 1 — إنشاء مشروع Firebase (مجاني 100%)

1. اذهب لـ: https://console.firebase.google.com
2. اضغط "Create a project"
3. اسم المشروع: `thanaweya-2026`
4. فعّل Google Analytics (اختياري)
5. اضغط "Continue" ثم "Create project"

---

### الخطوة 2 — تفعيل Authentication بجوجل

1. من القائمة الجانبية: **Build → Authentication**
2. اضغط "Get started"
3. اختر "Sign-in method"
4. فعّل **Google** — اضغط Enable ثم Save
5. أضف دومين موقعك في "Authorized domains"

---

### الخطوة 3 — تفعيل Firestore Database

1. من القائمة: **Build → Firestore Database**
2. اضغط "Create database"
3. اختر **"Start in test mode"** (تقدر تأمنه بعدين)
4. اختر region: `europe-west1` (الأقرب لمصر)

---

### الخطوة 4 — الحصول على Firebase Config

1. اضغط على أيقونة الويب `</>` في صفحة Project Settings
2. اسم التطبيق: `thanaweya-web`
3. **انسخ الـ config** — هتلاقي كالتالي:

```javascript
const firebaseConfig = {
  apiKey: "AIzaSy...",
  authDomain: "thanaweya-2026.firebaseapp.com",
  projectId: "thanaweya-2026",
  storageBucket: "thanaweya-2026.appspot.com",
  messagingSenderId: "123456789",
  appId: "1:123:web:abc"
};
```

---

### الخطوة 5 — تعديل الكود

افتح ملف `index.html` وابحث عن:

```javascript
const FIREBASE_CONFIG = {
  apiKey: "YOUR_API_KEY",
  ...
};
const ADMIN_EMAIL = "YOUR_ADMIN_EMAIL@gmail.com";
```

استبدل بمعلوماتك الحقيقية.

---

### الخطوة 6 — نشر الموقع على Firebase Hosting (رابط .web.app مجاني)

#### تثبيت Firebase CLI:
```bash
npm install -g firebase-tools
```

#### تسجيل الدخول:
```bash
firebase login
```

#### داخل مجلد الموقع:
```bash
firebase init hosting
```
- اختر مشروعك
- Public directory: `.` (نقطة)
- Single page app: `No`
- GitHub deploys: `No`

#### النشر:
```bash
firebase deploy
```

سيعطيك رابط مثل:
`https://thanaweya-2026.web.app`

---

### الخطوة 7 — ربط دومين مخصص (اختياري)

1. في Firebase Console → Hosting → "Add custom domain"
2. أدخل دومينك مثل: `thanawiya2026.com`
3. اتبع تعليمات DNS

---

### الخطوة 8 — لوحة التحكم (أنت فقط)

- سجل دخولك بنفس إيميلك اللي حطيته في `ADMIN_EMAIL`
- هيظهر تبويب "⚙️ لوحة التحكم" في الأعلى لك أنت بس
- تقدر تشوف عدد المستخدمين والإشعارات وترسل بث جماعي

---

### الخطوة 9 — تفعيل الإشعارات (Firebase Cloud Messaging)

1. Firebase Console → Project Settings → Cloud Messaging
2. انسخ Server Key
3. في الكود، أضف VAPID key في:
```javascript
messaging.getToken({ vapidKey: 'YOUR_VAPID_KEY' });
```

---

## الميزات الموجودة في الموقع

✅ عداد تنازلي بالثانوية والأزهرية (يومي + ساعي + دقيقي + ثانوي)
✅ عداد نهاية الامتحانات
✅ عداد بداية الجامعة
✅ جدول الثانوية العامة الكامل
✅ جدول الأزهرية الكامل
✅ خط الرحلة من الآن للجامعة
✅ تسجيل دخول بجوجل
✅ إشعارات يومية
✅ لوحة تحكم المصمم
✅ تصميم موبايل + كمبيوتر
✅ يعمل كـ PWA (تثبيت على الموبايل كأبلكيشن)
✅ وضع ليلي كامل
✅ اسم المصمم في الفوتر

---

## اسم المصمم
محمد العوضي شاهين
