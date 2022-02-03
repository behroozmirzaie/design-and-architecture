<!-- Output copied to clipboard! -->

<!-----

Yay, no errors, warnings, or alerts!

Conversion time: 0.208 seconds.


Using this Markdown file:

1. Paste this output into your source file.
2. See the notes and action items below regarding this conversion run.
3. Check the rendered output (headings, lists, code blocks, tables) for proper
   formatting and use a linkchecker before you publish this page.

Conversion notes:

* Docs to Markdown version 1.0β33
* Wed Feb 02 2022 22:03:53 GMT-0800 (PST)
* Source doc: Load Balancing
* This is a partial selection. Check to make sure intra-doc links work.
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
