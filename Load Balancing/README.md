<!-- Output copied to clipboard! -->

<!-----

Yay, no errors, warnings, or alerts!

Conversion time: 0.325 seconds.


Using this Markdown file:

1. Paste this output into your source file.
2. See the notes and action items below regarding this conversion run.
3. Check the rendered output (headings, lists, code blocks, tables) for proper
   formatting and use a linkchecker before you publish this page.

Conversion notes:

* Docs to Markdown version 1.0β33
* Thu Feb 03 2022 00:21:10 GMT-0800 (PST)
* Source doc: Load Balancing
----->


<p dir="rtl">
۱- منظور از Load Balancing چیست؟ </p>


<p dir="rtl">
Load balancing  تکنیک ساده ای برای توزیع load  در چندین ماشین یا cluster است. رایج ترین و ساده ترین الگوریتم برای Load balancing الگوریتم  Round Robin  است.  در این نوع Load balancing ، درخواست به ترتیب دایره‌ای تقسیم می‌شود تا مطمئن بشم که همه ماشین ها تعداد درخواست های هم اندازه ای (یکسان) دریافت میکنند و هیچ ماشینی load بیشتر یا کمتر نخواهد داشت. </p>


<p dir="rtl">
اهداف استفاده از Load Balancing:</p>




* بهینه سازی استفاده از منابع
* دستیابی به حداکثر توان عملیاتی
* به حداقل رساندن زمان پاسخگویی

<p dir="rtl">
رایج ترین تکنیک های Load Balancing در برنامه های مبتنی بر وب:</p>


<p dir="rtl">
اول) Round robin</p>


<p dir="rtl">
دوم) Session affinity or sticky session</p>


<p dir="rtl">
سوم) IP Address affinity</p>


<p dir="rtl">
۲- تکنیک Round robin چیست؟ </p>


<p dir="rtl">
یکی از ساده ترین روش ها برای توزیع درخواست های client بین گروهی از سرور هاست. زمانی که گروهی از سرور ها در دسترس نیستند round-robin درخواست client را به  سروری که نوبتش هست میفرسته. زمانی که به پایان لیستش برسه، load balancer این حلقه را تکرار میکنه. </p>


![](https://raw.githubusercontent.com/behroozmirzaie7/design-and-architecture/feature/add_load_balancing/Load%20Balancing/round-robin.png)

<p dir="rtl">
۳- برخی از محاسن Round Robin را توضیح دهید. </p>


<p dir="rtl">
مهم ترین سود استفاده از round-robin راحتی پیاده سازی اون هستش. اگرچه، همیشه دقیق ترین و کراامد ترین راه حل نیست. </p>


<p dir="rtl">
چون خیلی از round robin balancer ها فکر میکنند تمام سرور ها یکسان هستند.(همشون فعال هستند، همون load را مدیریت میکنند و ظرفیت ذخیره سازی و محاسباتی یکسانی دارند) </p>


<p dir="rtl">
۴- Sticky Session Load Balancing چیست؟ و  منظور از Session Affinity چیست؟</p>


<p dir="rtl">
Sticky session یا session affinity تکنیک دیگری از تکنیک های رایج Load Balancing است که به یک session کاربر نیاز دارد که همیشه توسط یک ماشین اختصاص داده شده(allocated machine)  ارائه شود. در یک برنامه Load Balanced  که در آن اطلاعات کاربر در session  ذخیره می‌شود، لازم است داده‌های session در دسترس همه ماشین‌ها باشد. برای جلوگیری از این امر میتوان همیشه درخواست های اون کاربر خاص روبه یک ماشین ارسال کرد. به محض ایجاد session  ماشین با یک session مرتبط می شود. تمام درخواست‌ها در یک session  خاص همیشه به ماشین مرتبط هدایت می‌شوند. این تضمین می‌کند که داده‌های کاربر فقط در یک دستگاه است و load  نیزshare می‌شود.</p>


<p dir="rtl">
این معمولا با استفاده از کوکی SessionId انجام می شود. کوکی برای اولین درخواست client ارسال می شود. و هر درخواست بعدی توسط client باید حاوی همان کوکی باشد تا session را شناسایی کند.</p>


<p dir="rtl">
مسائل مربوط به Sticky Session چیست؟</p>


<p dir="rtl">
مشکلات کمی وجود دارد که ممکن است باهاش مواجه شوید:</p>




* ممکن است مرورگر سرویس گیرنده (همون client) از کوکی ها پشتیبانی نکند و load balancer  شما نمی تواند تشخیص دهد که آیا درخواست متعلق به یک session است یا خیر. این مورد برای کاربرانی که از مرورگر های که مبتنی بر کوکی نیستند استفاده می کنند رفتار عجیبی ایجاد میکند.
* در صورتی که یکی از دستگاه ها از کار بیفتد یا از کار بیفتد، اطلاعات کاربر (که توسط آن دستگاه ارائه می شود) از بین می رود و راهی برای بازیابی جلسه کاربر وجود نخواهد داشت.
* در صورتی که ماشینی که اطلاعات کاربر بر روی اون دستگاه نگهداری (ارائه) میشود down بشه راهی برای بازیابی session کاربر وجود نخواهد داشت. 