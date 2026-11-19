# أبو حاتم v12 — تحويل التطبيق إلى APK

## الطريقة الأسهل (بدون Android Studio): GitHub
1. أنشئ حساب مجاني في github.com ثم مستودع جديد (New repository).
2. ارفع كل محتويات هذا المجلد (Add file ← Upload files)، مع مجلد `.github` المخفي.
3. من تبويب **Actions** ← **Build APK** ← **Run workflow**.
4. بعد 5 إلى 8 دقائق افتح العملية المكتملة ونزّل **abu-hatim-apk** من Artifacts، وفك الضغط لتجد `app-debug.apk`.
5. انقله للجوال وثبّته (فعّل «التثبيت من مصادر غير معروفة»).

## الطريقة الثانية: Android Studio
```
npm install
npx cap add android
npx @capacitor/assets generate --android
npx cap sync android
npx cap open android
```
ثم Build ← Build APK(s).

## ملاحظات
- الملف الناتج debug ويصلح للتثبيت المباشر. للنشر في Google Play تحتاج نسخة موقّعة (Release).
- البيانات محفوظة محليًا على الجوال، فصدّر نسخة احتياطية دوريًا من تبويب «التقارير والنسخ».
- لتعديل التطبيق عدّل `www/index.html` فقط.
