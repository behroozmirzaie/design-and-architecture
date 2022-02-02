<!-- Output copied to clipboard! -->

<!-----

Yay, no errors, warnings, or alerts!

Conversion time: 0.379 seconds.


Using this Markdown file:

1. Paste this output into your source file.
2. See the notes and action items below regarding this conversion run.
3. Check the rendered output (headings, lists, code blocks, tables) for proper
   formatting and use a linkchecker before you publish this page.

Conversion notes:

* Docs to Markdown version 1.0β33
* Wed Feb 02 2022 02:30:57 GMT-0800 (PST)
* Source doc: Caching
----->


<p dir="rtl">
۱- Caching چیست؟ </p>


<p dir="rtl">
در computing،  کش یک لایه ذخیره سازی داده با سرعت بالا است که زیر مجموعه ای از داده ها را ذخیره می کند.معمولاً ماهیت گذرا دارد، به طوری که درخواست‌های آینده برای آن داده‌ها سریع‌تر از آنچه که با دسترسی به مکان ذخیره‌سازی اولیه داده ممکن است، ارائه می‌شوند.ذخیره سازی به شما امکان می دهد تا به طور موثر از داده های بازیابی یا محاسبه شده قبلی استفاده مجدد کنید.</p>


<p dir="rtl">
۲- آیا Redis فقط یک کش است؟</p>


<p dir="rtl">
مانند کش کردن Redis امکان میدهد:</p>




* in memory key-value storage

<p dir="rtl">
برخلاف کش کردن: </p>




* پشتیبانی از چند نوع datatype مانند strings,hashes,lists, sets, sorted sets, bimaps, ..
* قابلیتی را میده که داده های که قصد کش کردن داریم را در physcial storage ذخیره کنیم(اگر نیازبود)
* از مدل pub-sub پشتیبانی می کند
* حافظه نهان Redis برای دسترسی بالا امکان replication را فراهم می کند(master/slave)
* از اسکریپت های فوق سریع LUA پشتیبانی می کند. زمان اجرای آن برابر با اجرای دستورات C است.
* می تواند در چندین instance از برنامه به اشتراک گذاشته شود

<p dir="rtl">
۳- Resultset Caching چیست؟</p>


<p dir="rtl">
Resultset Caching نتایج یک پرس و جو پایگاه داده را به همراه پرس و جو در برنامه ذخیره می کند. هر بار که یک صفحه وب یک پرس و جو ایجاد می کند، برنامه‌ها بررسی می‌کنند که آیا نتایج قبلاً ذخیره شده‌اند یا نه، و اگر هستند، به جای آن، آنها را از مجموعه داده‌های درون حافظه بیرون می‌کشند. application هنوز باید صفحه را رندر کند.</p>

