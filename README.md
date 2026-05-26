# عيدية — لعبة العيلة في العيد

لعبة HTML standalone جاهزة للنشر على Vercel.

## النشر — أسهل طريقة (Drag & Drop)

1. ادخل على https://vercel.com وسجّل دخول بـ GitHub أو Email
2. من الـ dashboard اضغط **Add New → Project**
3. تحت "Import Git Repository" هتلاقي خيار **"Deploy from your machine"** أو استخدم Vercel CLI تحت
4. اسحب الفولدر ده كامل (مش الـ ZIP، الفولدر بعد ما تفكّه)
5. هيطلعلك Preview، اضغط **Deploy**
6. خلال 10-20 ثانية الموقع شغّال على لينك زي `eidiyah-game.vercel.app`

## النشر عن طريق Vercel CLI (أسرع طريقة)

افتح terminal في الفولدر ده وشغّل:

```bash
npm i -g vercel
vercel
```

هيسألك:
- Set up and deploy? → **Y**
- Which scope? → اختار حسابك
- Link to existing project? → **N**
- Project name? → `eidiyah-game` (أو أي اسم)
- Code directory? → `./` (اضغط Enter)
- Override settings? → **N**

خلاص. هيطلعلك اللينك على طول.

للنشر النهائي على production:
```bash
vercel --prod
```

## النشر عن طريق GitHub (لو عايز auto-deploy)

1. اعمل repo جديد على GitHub (مثلاً `eidiyah-game`)
2. ارفع محتويات الفولدر ده:
   ```bash
   git init
   git add .
   git commit -m "Initial commit"
   git remote add origin https://github.com/USERNAME/eidiyah-game.git
   git push -u origin main
   ```
3. في Vercel: **Add New → Project → Import** واختار الـ repo
4. اضغط Deploy

دلوقتي أي push على `main` هيعمل deploy تلقائي.

## ربط دومين خاص

Settings → Domains → Add → اكتب الدومين (مثلاً `eidiyah.com`)
Vercel هيديك DNS records تحطها عند مزوّد الدومين بتاعك.

## ملفات الفولدر

- `index.html` — اللعبة كاملة (1.8 MB، كل حاجة inline)
- `vercel.json` — إعدادات الـ caching والـ security headers
- `README.md` — الملف ده
