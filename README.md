📝 QH VisionX Notepad v2

Professional Persian RTL Notepad

یک برنامه حرفه‌ای، سریع و سبک برای یادداشت‌برداری فارسی و راست‌به‌چپ که با HTML + CSS + JavaScript ساخته شده و بدون نیاز به Backend اجرا می‌شود.

🌐 Live Demo:
https://qaisamin.github.io/qh-visionx-notepad/

📦 Repository:
https://github.com/qaisamin/qh-visionx-notepad

---

✨ امکانات

- 📝 ایجاد و مدیریت چندین یادداشت
- 🔎 جستجوی سریع بین یادداشت‌ها
- ⭐ افزودن یادداشت به Favorites
- 🗑️ انتقال به Trash
- ↩️ بازیابی یادداشت‌های حذف‌شده
- ⧉ ایجاد نسخه کپی از یادداشت
- ✏️ ویرایش متن Rich Text
- Bold / Italic / Underline
- "Heading"
- "Quote"
- Bullet List
- Numbered List
- 🔗 افزودن لینک
- ↶ Undo
- ↷ Redo
- 💾 ذخیره خودکار
- 🌙 Dark Mode
- ☀️ Light Mode
- 📋 Copy
- 📥 خروجی TXT
- 📝 خروجی Markdown
- 💾 Backup به JSON
- ♻️ Restore از JSON
- 🖨️ Print
- 📊 شمارش کلمات و حروف
- ⌨️ Keyboard Shortcuts
- 📱 طراحی Responsive برای موبایل
- 🇦🇫 رابط فارسی و RTL
- 📲 PWA Ready
- 🔐 ذخیره محلی با LocalStorage
- ⚡ بدون Backend
- 🚀 آماده GitHub Pages
- 🚀 آماده Netlify

---

🛠️ تکنولوژی‌ها

HTML5
CSS3
JavaScript
LocalStorage
Web App Manifest
Responsive Design
RTL / Persian UI

هیچ Framework یا Library اجباری برای اجرای پروژه وجود ندارد.

---

📁 ساختار پروژه

qh-visionx-notepad/
│
├── index.html
├── style.css
├── app.js
├── manifest.json
├── favicon.svg
├── .nojekyll
└── README.md

---

💾 ذخیره اطلاعات

QH VisionX Notepad v2 از LocalStorage مرورگر برای ذخیره یادداشت‌ها استفاده می‌کند.

بنابراین:

- نیاز به حساب کاربری ندارد.
- نیاز به Server ندارد.
- نیاز به Database ندارد.
- یادداشت‌ها در مرورگر همان دستگاه ذخیره می‌شوند.

«توجه: LocalStorage به‌صورت خودکار بین دستگاه‌های مختلف Sync نمی‌شود.»

برای همگام‌سازی بین موبایل، کامپیوتر و سایر دستگاه‌ها می‌توان در نسخه آینده Backend و Cloud Sync اضافه کرد.

---

🔐 حریم خصوصی

در نسخه فعلی، محتوای یادداشت‌ها به Backend ارسال نمی‌شود و در فضای ذخیره‌سازی محلی مرورگر نگهداری می‌شود.

با این حال، کاربران باید برای اطلاعات بسیار حساس از دستگاه و مرورگر امن استفاده کنند.

---

⌨️ میانبرهای صفحه‌کلید

Shortcut| عملکرد
"Ctrl + N"| یادداشت جدید
"Ctrl + S"| ذخیره
"Ctrl + K"| جستجو
"Esc"| بستن منو

در macOS می‌توان از "Command" به‌جای "Ctrl" استفاده کرد.

---

🌙 Dark / Light Mode

برنامه دارای دو حالت نمایش است:

🌙 Dark Mode
☀️ Light Mode

انتخاب کاربر در مرورگر ذخیره می‌شود.

---

📦 Backup & Restore

کاربر می‌تواند تمام یادداشت‌ها را به صورت فایل JSON پشتیبان‌گیری کند.

نمونه:

qh-visionx-notepad-backup.json

سپس می‌توان فایل پشتیبان را برای بازیابی اطلاعات استفاده کرد.

---

🚀 اجرای محلی

Repository را دریافت کنید:

git clone https://github.com/qaisamin/qh-visionx-notepad.git

سپس وارد پوشه شوید:

cd qh-visionx-notepad

و "index.html" را در مرورگر باز کنید.

---

🌐 GitHub Pages

این پروژه برای GitHub Pages آماده است.

تنظیمات:

Settings
   ↓
Pages
   ↓
Build and deployment
   ↓
Deploy from a branch
   ↓
Branch: main
   ↓
Folder: / (root)

سایت:

https://qaisamin.github.io/qh-visionx-notepad/

---

🚀 Netlify

پروژه را می‌توان مستقیماً در Netlify Deploy کرد.

پوشه پروژه را انتخاب کنید یا Repository GitHub را به Netlify متصل کنید.

هیچ Build Command خاصی نیاز نیست.

Build command: None
Publish directory: /

---

📱 PWA

پروژه دارای:

manifest.json

است و ساختار آن برای تبدیل به Progressive Web App آماده شده است.

در نسخه‌های آینده می‌توان موارد زیر را اضافه کرد:

- Service Worker
- Offline Mode
- Install Prompt
- App Icon
- Full Offline Application

---

🔮 Roadmap

v2.1

- [ ] Service Worker
- [ ] Offline کامل
- [ ] نصب مستقیم به‌عنوان App
- [ ] Drag & Drop برای یادداشت‌ها
- [ ] Tag Manager پیشرفته
- [ ] Folder Manager

v3.0

- [ ] حساب کاربری
- [ ] Cloud Sync
- [ ] Supabase
- [ ] همگام‌سازی چند دستگاه
- [ ] اشتراک‌گذاری یادداشت
- [ ] لینک خصوصی برای Notes

آینده

- [ ] AI Writing Assistant
- [ ] خلاصه‌سازی با AI
- [ ] ترجمه
- [ ] اصلاح املایی فارسی
- [ ] تبدیل Voice → Text
- [ ] OCR
- [ ] همکاری هم‌زمان
- [ ] Encryption پیشرفته

---

🎨 Brand

QH VisionX

محصول:

QH VisionX Notepad

نسخه:

v2.0

---

📄 License

این پروژه در حال حاضر بدون تعیین License عمومی منتشر شده است.

برای استفاده تجاری یا بازنشر، قبل از اضافه‌کردن License رسمی، شرایط مالک پروژه را بررسی کنید.

---

👨‍💻 Project

QH VisionX

GitHub:

https://github.com/qaisamin

Repository:

https://github.com/qaisamin/qh-visionx-notepad

---

⭐ Support

اگر این پروژه برای شما مفید است، می‌توانید Repository را در GitHub ⭐ Star کنید.

QH VisionX — Smart Tools for the Future.
