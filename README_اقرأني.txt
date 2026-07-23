SmartCrowd Guardian — حارس الحشود الذكي
=========================================
تطبيق ويب قابل للتثبيت (PWA) — نسخة الاستضافة

لماذا هذه الحزمة؟
----------------
المتصفحات لا تسمح بتثبيت أي تطبيق ويب عندما يُفتح كملفٍّ محلي (file://).
شرط التثبيت أن يُفتح التطبيق عبر رابط ويب آمن (https://).
هذه الحزمة تحتوي كل ما يلزم ليصبح التطبيق قابلاً للتثبيت بنقرة واحدة على
الجوال والحاسوب فور رفعها على أي استضافة تدعم https.

محتويات الحزمة:
  index.html                ← التطبيق
  manifest.webmanifest      ← بيانات التطبيق (الاسم، الأيقونات، وضع standalone)
  sw.js                     ← خدمة العمل (offline + شرط التثبيت)
  icon-192.png / icon-512.png / icon-maskable-512.png / apple-touch-icon.png

=========================================
الطريقة الأسرع (بدون حساب، بدون برمجة): Netlify Drop
=========================================
1) افتح المتصفح على:  https://app.netlify.com/drop
2) اسحب مجلد «SmartCrowd_Guardian_App» كاملاً وأفلته في الصفحة.
3) خلال ثوانٍ ستحصل على رابط مثل:  https://اسم-عشوائي.netlify.app
4) افتح هذا الرابط على جوالك أو حاسوبك:
   • أندرويد (Chrome): القائمة (⋮) ← «تثبيت التطبيق».
   • آيفون/آيباد (Safari): زر المشاركة ⬆️ ← «إضافة إلى الشاشة الرئيسية».
   • حاسوب (Chrome/Edge): أيقونة التثبيت ⊕ في نهاية شريط العنوان.

=========================================
بديل: GitHub Pages
=========================================
1) أنشئ مستودعاً جديداً على GitHub وارفع محتويات هذه الحزمة.
2) Settings ← Pages ← اختر الفرع main والمجلد /(root) ← Save.
3) سيعطيك رابط https://اسم-المستخدم.github.io/اسم-المستودع/
4) افتح الرابط واتبع خطوات التثبيت أعلاه.

=========================================
بديل للتجربة محلياً على حاسوبك (اختياري)
=========================================
داخل مجلد الحزمة شغّل أحد الأمرين ثم افتح http://localhost:8000
  Python:  python -m http.server 8000
  Node:    npx serve .
ملاحظة: localhost يُعامَل معاملة الرابط الآمن، فيظهر خيار التثبيت.

--------------------------------------------------------------
القلب الرياضي المعتمد: قانون حفظ LWR + مخطط Godunov المصحّح +
مصدر/مصرف محدود سعوياً — يضمن ρ∈[0,6] وتدقيق كتلة دقيق.
مبني على بحث «دراسة رياضية شاملة لنموذج طائرة حارس الحشود الذكية» — جامعة القصيم.
--------------------------------------------------------------


SmartCrowd Guardian (English)
=========================================
Installable web app (PWA) — hosting bundle.

Browsers do NOT allow installing a web app opened as a local file (file://).
Installation requires opening the app over a secure link (https://).
This bundle makes the app one-click installable on phone and laptop once
you put it on any static host with https.

Fastest way (no account, no coding): Netlify Drop
  1) Open  https://app.netlify.com/drop
  2) Drag the whole "SmartCrowd_Guardian_App" folder onto the page.
  3) You get a https://something.netlify.app link within seconds.
  4) Open that link:
     - Android (Chrome): menu (⋮) -> "Install app".
     - iPhone/iPad (Safari): Share ⬆️ -> "Add to Home Screen".
     - Desktop (Chrome/Edge): install icon ⊕ at the end of the address bar.

Alternative: GitHub Pages, or run locally with `python -m http.server 8000`
and open http://localhost:8000 (localhost counts as secure).
