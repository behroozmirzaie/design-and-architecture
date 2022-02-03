<!-- Output copied to clipboard! -->

<!-----

Yay, no errors, warnings, or alerts!

Conversion time: 0.251 seconds.


Using this Markdown file:

1. Paste this output into your source file.
2. See the notes and action items below regarding this conversion run.
3. Check the rendered output (headings, lists, code blocks, tables) for proper
   formatting and use a linkchecker before you publish this page.

Conversion notes:

* Docs to Markdown version 1.0β33
* Thu Feb 03 2022 12:58:29 GMT-0800 (PST)
* Source doc: Databases
----->


<p dir="rtl">
۱- نرمال سازی چیست؟ </p>


<p dir="rtl">
نرمال سازی در زمان طراحی پایگاه داده از داده های تکراری و اضافه جلوگیری می کند. اگر یک اطلاعات خاص در چند جا تکرار شده باشد این امکان وجود داره که یکی از اون جداول تغییر کند ولی سایر جدول ها آپدیت نشوند و این باعث بروز خطا خواهد شد. نرمال سازی از سطح فرم ۱ تا سطح فرم ۵ هستش. و هر کدام  از این فرم ها نحوه حل یک مشکل را تشریح می کند. </p>


<p dir="rtl">
وجود یک پایگاه داده ای که خطاهای نرمال سازی داشته باشد (normalization errors) ، خطر ورود داده های نامعتبر یا خراب به پایگاه داده را باز می کند. از آنجایی که داده‌ها «برای همیشه زنده هستند»، خلاص شدن از شر داده‌های مشکل دار  زمانی که برای اولین بار وارد پایگاه داده می‌شوند، دشوار است.</p>



---

<p dir="rtl">
۲- مزایای NoSQL نسبت به RDBMS سنتی چیست؟</p>


<p dir="rtl">
مزایای NoSQL نسبت به RDBMS ها عبارتند از:</p>


<p dir="rtl">
از داده های نیمه ساختاریافته و داده های فرار پشتیبانی می کند</p>


<p dir="rtl">
اسکیما ندارد (schema)</p>


<p dir="rtl">
توان خواندن/نوشتن بسیار بالاست</p>


<p dir="rtl">
مقیاس پذیری افقی را می توان به راحتی به دست آورد (Horizontal scalability)</p>


<p dir="rtl">
از داده های بزرگ در حجم ترابایت و پتا بایت پشتیبانی می کند</p>


<p dir="rtl">
در داده های بزرگ ابزار از ابزار تحلیلی به خوبی پشتیبانی می کند.</p>


<p dir="rtl">
می توان در مکانیزم های  سخت افزاری ارزان تر استفاده کرد </p>


<p dir="rtl">
گزینه ذخیره سازی درون حافظه برای افزایش عملکرد پرس و جوها در دسترس است ( in memory caching)</p>


<p dir="rtl">
چرخه عمر توسعه سریعتر برای توسعه دهندگان (Faster development life cycles for developers)</p>


<p dir="rtl">
مزایایی استفاده از RDBMS ها نسبت به NoSQL ها:</p>


<p dir="rtl">
تراکنش ها با خصوصیات ACID و atomicity, consistency , isolation & durability</p>


<p dir="rtl">
پایبندی به Schema </p>


<p dir="rtl">
مدیریت query  در real time  (در صورتی که  اندازه داده ها کمتر از 10 ترا بایت باشد.)</p>


<p dir="rtl">
اجرای query های پیچیده شامل join و group by </p>



---
