<!-- Output copied to clipboard! -->

<!-----

Yay, no errors, warnings, or alerts!

Conversion time: 0.293 seconds.


Using this Markdown file:

1. Paste this output into your source file.
2. See the notes and action items below regarding this conversion run.
3. Check the rendered output (headings, lists, code blocks, tables) for proper
   formatting and use a linkchecker before you publish this page.

Conversion notes:

* Docs to Markdown version 1.0β33
* Thu Feb 03 2022 13:10:30 GMT-0800 (PST)
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




* از داده های نیمه ساختاریافته و داده های فرار پشتیبانی می کند
* اسکیما ندارد (schema)
* توان خواندن/نوشتن بسیار بالاست
* مقیاس پذیری افقی را می توان به راحتی به دست آورد (Horizontal scalability)
* از داده های بزرگ در حجم ترابایت و پتا بایت پشتیبانی می کند
* در داده های بزرگ ابزار از ابزار تحلیلی به خوبی پشتیبانی می کند.
* می توان در مکانیزم های  سخت افزاری ارزان تر استفاده کرد
* گزینه ذخیره سازی درون حافظه برای افزایش عملکرد پرس و جوها در دسترس است ( in memory caching)
* چرخه عمر توسعه سریعتر برای توسعه دهندگان (Faster development life cycles for developers)

<p dir="rtl">
مزایایی استفاده از RDBMS ها نسبت به NoSQL ها:</p>




* تراکنش ها با خصوصیات ACID و atomicity, consistency , isolation & durability
* پایبندی به Schema
* مدیریت query  در real time  (در صورتی که  اندازه داده ها کمتر از 10 ترا بایت باشد.)
* اجرای query های پیچیده شامل join و group by


---

<p dir="rtl">
۳- تفاوت DDL - Data Definition Language و DML -  Data manipulation Language چیست؟ </p>


<p dir="rtl">
DDL: دستوراتی هستند که برای تعریف پایگاه داده استفاده می شوند. CREATE، ALTER، DROP و TRUNCATE برخی از دستورات رایج DDL هستند.</p>


<p dir="rtl">
DML:  دستوراتی هستند که برای دستکاری داده ها استفاده می شوند. INSERT، UPDATE و DELETE برخی از دستورات رایج DML هستند.</p>



---

<p dir="rtl">
۴- خصوصیات ACID را توضیح دهید. </p>


<p dir="rtl">
اول) Atomicity: این قانون همه یا هیچ را برای تغییرات پایگاه داده تضمین می کند.(all-or-none)</p>


<p dir="rtl">
دوم) Consistency: مقادیر داده در سرتاسر پایگاه داده یکسان است.</p>


<p dir="rtl">
سوم) Isolation: گفته می شود که دو transactions مستقل از یکدیگر هستند.</p>


<p dir="rtl">
چهارم) Durability: داده ها حتی در زمان خرابی سرور از بین نمی روند.</p>



---
