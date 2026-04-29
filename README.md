# أبيان كابيتال — صفحة التصويت
## ملفات المشروع

```
app_vote_hobb.html   ← الصفحة الرئيسية
logo_header.png      ← شعار الهيدر
logo_nav.png         ← شعار شريط التنقل
votes.json           ← نسخة احتياطية من قاعدة البيانات (الأصل في GitHub Gist)
```

---

## خطوات النشر على GitHub Pages

### الخطوة 1 — تحديث Gist بالملف الصحيح

1. اذهب إلى: https://gist.github.com/emaderre-hue/1fae2f1477560df32188b623bbecbc5d
2. اضغط **Edit**
3. تأكد أن اسم الملف `votes.json` والمحتوى:
   ```json
   {"votes":{"1":0,"2":0,"3":0,"4":0,"5":0,"6":0,"7":0},"voters":[]}
   ```
4. اضغط **Update public gist**

---

### الخطوة 2 — رفع الملفات إلى GitHub Repository

1. اذهب إلى: https://github.com/emaderre-hue/myy-site
2. اضغط **Add file** → **Upload files**
3. ارفع الملفات الثلاثة:
   - `app_vote_hobb.html`
   - `logo_header.png`
   - `logo_nav.png`
4. في حقل Commit message اكتب: `update voting page`
5. اضغط **Commit changes**

---

### الخطوة 3 — تفعيل GitHub Pages (إن لم يكن مفعّلاً)

1. في الـ repository، اضغط **Settings**
2. من القائمة الجانبية اضغط **Pages**
3. تحت **Source** اختر **Deploy from a branch**
4. اختر **main** branch و **/ (root)**
5. اضغط **Save**
6. انتظر دقيقة ثم افتح:
   `https://emaderre-hue.github.io/myy-site/app_vote_hobb.html`

---

## كيف يعمل النظام

- **عند فتح الصفحة**: تُحمَّل الأصوات من GitHub Gist مباشرة
- **عند التصويت**: يُحفَظ الصوت في Gist وتتحدث البيانات عبر كل الأجهزة
- **الأدمن**: كلمة المرور `admin2025` — تُتيح رؤية النتائج وحذف/إعادة تعيين الأصوات

---

## تغيير كلمة مرور الأدمن

في ملف `app_vote_hobb.html` ابحث عن:
```javascript
const ADMIN_PASS = 'admin2025';
```
وغيّر القيمة.

---

## ملاحظة أمان

الـ Token الموجود في الكود له صلاحية Gist فقط.
لتجديده: https://github.com/settings/tokens
