---

layout: col-document
title: شیوه‌های کدنویسی امن
tags: SCP-QRG
document: راهنمای کدنویسی امن

---

{% include breadcrumb.html %}
# پیوست دوم: واژه‌نامه

**مورد سوء استفاده:** شرحی از استفاده‌های عمدی و
  غیرعمدی از نرم‌افزار. موارد سوء استفاده باید
  فرضیات طراحی سیستم را به چالش بکشند.

**کنترل دسترسی:** مجموعه‌ای از کنترل‌هایی که به کاربر یا
  موجودیت دیگر، دسترسی به سیستم را به صورت مجاز یا غیرمجاز می‌دهند.
  این دسترسی معمولا بر اساس نقش‌های سلسله مراتبی یا مجوزهای فردی
  داخل یک نقش است. این موضوع شامل تعاملات سیستم با سیستم نیز می‌شود.

**غیرفعال‌سازی حساب:** غیرفعال‌سازی حساب پس از تعداد تلاش‌های نامعتبر ورود
  به عنوان مثال پنج تلاش معمول است. حساب باید برای مدت زمانی کافی
  غیرقابل دسترسی شود تا از حملات جستجوری فراگیر جلوگیری کند
  اما این زمان به گونه‌ای باید تنظیم گردد که منجر بخ رخداد
  منع‌سرویس و عدم دسترس‌پذیری معمول نشود.

**احرازهویت:** مجموعه‌ای از کنترل‌ها که در راستای تایید هویت
  کاربر یا موجودیت دیگری که در تعامل با نرم‌افزار است استفاده می‌شود.

  پاسخ‌های مربوط به احرازهویت ناموفق نباید نشان دهد کدام قسمت از
  اطلاعات وارد شده در فرایند احرازهویت نادرست بوده است.
  برای مثال به جای پیام نام‌کاربری نامعتبر یا گذرواژه نامعتبر فقط از
  نام‌کاربری و یا رمزعبور نامعتبر برای هردو استفاده کنید.
  پاسخ‌های خطا باید هم در نمایش و هم در کد واقعا یکسان باشند.

**دسترس‌پذیری:** معیاری برای دسترسی و قابلیت استفاده از یک سیستم.

**خطاهای محاسباتی:** با درک نحوه عملکرد زبان برنامه‌نویسی و
  نحوه تعامل آن با محاسبات عددی، از خطاهای محاسباتی جلوگیری کنید.
  به تناقضات در مباحثی همچون دقت به اختلافات اندازه بایت، دقت اندازه‌گیری،
  تمایز‌های امضاء دار و بدون امضاء، تبدیل انواع داده‌ها، محاسبات غیر عددی
  و نحوه کارکرد زبانتان با اعدادی که بسیار بزرگ یا کوچک هستند توجه کنید.

**هم‌نوع کردن یا متعارف‌سازی:** برای کاهش انواع متعدد و مختلف انکد کردن
  و نمایش داده به فرمی ساده و مشترک.

**امنیت ارتباطات:** مجموعه‌ای از کنترل‌ها که کمک می‌کند
  اطمینان حاصل کنیم نرم‌افزار ارسال و دریافت
  اطلاعات را به شیوه‌ای امن انجام می دهد.

**محرمانگی:** برای اطمینان از اینکه اطلاعات فقط برای اشخاص مجاز افشاء می‌شود.

**انکد کردن داده‌های خروجی:**
  انکد کردن داده‌های خروجی بر اساس نحوه استفاده از آن توسط برنامه.
  شیوه‌های پیاده‌سازی بر اساس نحوه استفاده از خروجی متفاوت است.
  اگر داده قرار است در سمت کاربر نمایش داده شود مثلا در قالب کد‌های
  HTML, CSS یا Javascript
  می‌توانید از 
  HTML entity encoding 
  استفاده کنید ولی این موضوع در همه‌ی موارد کار نکند.
  همچنین لازم است داده و نحوه انکد کردن آن را در کوئری‌هایی نظیر
  SQL و XML و LDAP
  در نظر داشته باشید.

**جعل درخواست میان‌سایتی (CSRF):**
  یک وب‌سایت یا برنامه خارجی، یک کلاینت را مجبور می‌کند تا درخواست
  ناخواسته‌ای را به برنامه دیگری که در آن نشست فعال دارد، ارسال کند.
  زمانی برنامه‌ها به این مورد آسیب‌پذیر هستند که از آدرس‌ها و پارامترهای
  شناخته شده یا قابل پیش‌بینی استفاده کنند و مکانیزم پیاده‌سازی شده برای
  نشست به گونه‌ای باشد که مرورگر کاربر به صورت خودکار تمامی اطلاعات مربوط به
  نشست را در درخواست‌های سایت آسیب‌پذیر ارسال کند. مانند مکانیزم کوکی

**شیوه‌های رمزنگاری:** مجموعه‌ای از کنترل‌ها که تضمین می‌کنند
  عملیات رمزنگاری در بنامه به صورت ایمن مدیریت می‌شوند.

**محافظت از اطلاعات:** مجموعه‌ای از کنترل‌ها که
  کمک میکند از ذخیره‌سازی اطلاعات به شیوه‌ای امن
  توسط برنامه‌کاربردی اطمینان حاصل شود.

**امنیت پایگاه‌داده:** مجموعه‌ای از کنترل‌ها که اطمینان می‌دهد
  نرم‌افزار به شیوه‌ای امن با پایگاه‌داده تعامل دارد و
  پایگاه‌داده به طور امن پیکربندی شده است.

**مدیریت خطا و رویدادنگاری:** مجموعه‌ای از روش‌ها که اطمینان حاصل می‌کند
  برنامه به طور ایمن خطاها را مدیریت می‌کند و 
  ثبت رویداد‌ها به شکل صحیح صورت می‌گیرد.

**اکسپلویت:** بهره‌برداری از یک آسیب‌پذیری است.
  به طور معمول این یک اقدام آگاهانه است که طراحی شده تا با بهره‌گیری
  از یک آسیب‌پذیری، کنترل‌های امنیتی نرم‌افزار را به خطر بیاندازد.

**مدیریت فایل:** مجموعه‌ای از کنترل‌ها که تعامل بین کد و
  سایر فایل‌های سیستم را پوشش می‌دهد.

**شیوه‌های عمومی کدنویسی:** مجموعه‌ای از کنترل‌ها که رویه‌های کدنویسی
را پوشش می‌دهند که به راحتی در سایر دسته‌های دیگر قرار نمی‌گیرند.

**کاراکتر‌های خطرناک:** هرگونه کاراکتر یا نمایش انکد شده از آن
  که منجر به اجرای عملیات خاصی خارج از چیزی که برنامه برای آن تعبیه شده است
  گردد و تفسیر آن در برنامه باعث رخداد رویه‌ای خارج از قاعده شود.
  این کاراکتر‌ها ممکن است برای موارد زیر مورد استفاده قرار بگیرند:

  * تغییر ساختار کد یا عبارات موجود
  * درج کد جدید و ناخواسته
  * تغییر مسیرها
  * ایجاد نتایج غیرمنتظره از عملکردها یا روال‌های برنامه
  * ایجاد خطا
  * به خطر انداختن سایر سیستم‌های ذیل سرور اصلی

  اگر هریک از کاراکتر‌های خطرناک باید به عنوان ورودی مجاز باشند،
  اطمینان حاصل کنید کنترل‌های اضافی مانند انکد کردن خروجی، رابط‌های
  برنامه‌نویسی امن و... برای مدیریت شیوه انتقال و تعامل با این کاراکتر‌ها
  پیاده‌سازی شده باشند. نمونه‌هایی از برخی کاراکتر‌های خطرناک رایج عبارتند از:
  > \< \> \" \' % ( ) & + \\ \\\' \\\"
  
  * کاراکتر‌های خط جدید را بررسی کنید
    %0d, %0a, \\r, \\n
  * کاراکتر‌های تغییر مسیر یا تاثیر گذار در آدرس دهی را بررسی کنید
    (../ یا ..\\)
    در مواردی که استانداردهای بسط داده شده‌ی
    UTF-8 
    جزو ورودی‌های قابل قبول تعریف شده، موارد آدرس‌دهی معادل زیر را نیز بررسی کنید:
    %c0%ae%c0%ae/

**HTML Entity انکد کردن:** فرآیند جایگزینی برخی از کاراکتر‌های
  ASCII
  با معادل آن در
  HTML
  به عنوان مثال این شیوه انکد کردن می‌تواند علامت کوچکتر را
  <  با  &lt;
  جایگزین کند. این موارد در اکثر مفسر‌ها، به ویژه مرورگر‌ها،
  بی‌اثر هستند که میتواند حملات سمت کاربر را کاهش دهد.

**تاثیر:** اندازه‌گیری اثر منفی وقوع یک رویداد نامطلوب بر کسب و کار.
  نتیجه سوء استفاده از یک آسیب‌پذیری چه خواهد بود.

**اعتبارسنجی ورودی‌ها:** مجموعه‌ای از کنترل‌ها که ویژگی‌های همه داده‌های ورودی
  را بررسی و تایید می‌کند به گونه‌ای که داده‌ها مطابق چیزی باشند که
  در برنامه‌کاربردی مربوطه انتظار می‌رود. به عنوان مثال نوع داده، طول
  قابل قبول، محدوده مجاز آن، کاراکتر‌های قابل قبول و اینکه
  شامل کاراکتر‌های خطرناک شناخته شده نباشند.

**یکپارچگی:** حصول اطمینان از اینکه اطلاعات دقیق، کامل
  و معتبر است و توسط یک اقدام غیرمجاز تغییر نکرده است.

**رویدادنگاری:** این موضوع می‌بایست شامل موارد زیر باشد:

  ۱. مهر زمانی از اجزاء قابل اعتماد سیستم
  ۲. درجه‌بندی شدت برای هر رویداد
  ۳. برچسب‌گذاری رویداد‌های امنیتی، در صورتی که با سایر رویدادها مخلوط شده باشند
  ۴. هویت حساب‌کاربری که باعث این رویداد شده است
  ۵. IP مرتبط با درخواست
  ۶. نتیجه رویداد - موفقیت/شکست
  ۷. شرح واقعه

  حملاتی نظیر امتحان کردن یک رمزعبور ثابت برای حساب‌کاربری‌های مختلف
  شیوه‌ای است که در راستای دور زدن قفل شدن یک حساب‌کاربری خاص بکار می‌رود.
  این موضوع در زمانی رخ می‌دهد که شناسه‌های کاربری قابل مشاهده و یا حدس زدن هستند.
  توصیه می‌شود نظارت برای شناسایی اینگونه حملات داشته باشید.

**مدیریت حافظه:** مجموعه‌ای از کنترل‌ها که به نحوه‌ی 
استفاده از حافظه و بافر می‌پردازند.

**کاهش تاثیر:** اقداماتی که برای کاهش شدت یک آسیب‌پذیری انجام می‌شود.
  این اقدامات می‌تواند شامل حذف آسیب‌پذیری، ایجاد شرایطی برای سخت‌تر شدن
  بهره‌برداری از آسیب‌پذیری، یا کاهش تاثیر منفی بهره‌برداری موفق از آن باشد.

**احرازهویت چندعاملی (MFA):** یک نوع فرایند احرازهویت که
  کاربر را ملزم به تولید و استفاده از چند نوع اعتبارنامه متمایز می‌کند.
  به طور معمول این موضوع بر اساس موارد زیر است:

  * چیزی که تحت اختیار دارند نظیر تلفن همراه
  * چیزی که می‌دانند، مثلا یک کد
  * چیزی که هستند، به عنوان مثال اطلاعات بیولوژیکی نظیر اثر انگشت

**انکد کردن خروجی:** مجموعه‌ای از کنترل‌ها که به استفاده از انکد کردن
  برای اطمینان از ایمن بودن داده خروجی برنامه می‌پردازد.

**کوئری‌های پارامتری:**
  کوئری مورد استفاده خود را از داده‌هایی که قرار است جایگذاری شوند جدا نمایید.
  ساختار کوئری در بخش‌هایی قرار است با داده‌های شما تکمیل گردد.
  شیوه صحیح این امر بدین صورت است که کوئری مربوطه و داده‌هایی که قرار است
  در آن جایگذاری شوند، به صورت جداگانه برای پایگاه‌داده ارسال شوند.
  ابتدا کوئری برای پایگاه‌داده ارسال می‌شود و آماده می‌شود، سپس پارامتر‌های مربوطه
  ارسال و جایگذاری می‌شوند. اینگونه تفکیک پارامتر‌ها از کوئری برای پایگاه‌داده
  قابل انجام خواهد بود.

**پیچیدگی رمزعبور:** 
  الزامات پیچیدگی رمزعبور که توسط خط‌مشی یا مقررات تعیین شده است.
  اطلاعات مورد استفاده در احرازهویت می‌بایست از پیچیدگی کافی برخوردار باشند
  تا در مقابل حملاتی که معمولا قابل اجرا هستند مقاوم باشند.
  به عنوان مثال لزوم بر استفاده از حروف الفبا به همراه اعداد و/یا کاراکتر‌های خاص.

**طول رمزعبور:** الزامات طول رمزعبور که توسط سیاست یا مقررات تعیین می‌شود.
  به طور معمول استفاده از رمزعبور هشت کاراکتری متداول است اما شانزده 
  کاراکتر ایمن‌تر است. همچنین توصیه می‌شود از عبارات چندکلمه‌ای استفاده گردد.

**ورود‌های دائمی**: ورودهای دائمی و پایدار را ممنوع کنید و
  خاتمه اعتبار نشست را به صورت دوره‌ای تنظیم نمایید، حتی زمانی که نشست فعال است.
  اهمیت این موضوع برای برنامه‌هایی که از اتصالات شبکه‌ای قدرتمند پشتیبانی می‌کنند یا
  به سیستم‌های حیاتی متصل می‌شوند دوچندان است.
  زمان خاتمه اعتبار آن می‌بایست از الزامات کسب و کار پشتیبانی کرده و کاربر
  باید اعلان کافی برای کاهش اثرات منفی دریافت کند.

**به‌روزرسانی ایمن:** روشی برای به‌روزرسانی برنامه از منابع معتبر.
  اگر برنامه از به‌روزرسانی‌های خودکار استفاده می‌کند، از امضاهای رمزنگاری
  استفاده کنیداطمینان حاصل نمایید برنامه‌کاربردی شما آن امضا را تایید می‌کند.
  همچنین از کانال‌های رمزنگاری شده برای انتقال کد از سرور میزبان استفاده کنید.

**تطهیر داده:** فرایندی است که
  با حذف، جایگزینی، کذگذاری یا گریز از کاراکترها، داده‌هایی که
  ممکن است آسیب‌زا باشند را ایمن می‌کند.

**کنترل‌های امنیتی:** اقداماتی که در آن
  آسیب‌پذیری‌های احتمالی را کاهش می‌دهد و اطمینان حاصل می‌کند
  که نرم‌افزار تنها به شیوه‌ی مورد نظر عمل می‌کند.

**الزامات امنیتی:** مجموعه‌ای از
  الزامات طراحی و عملکردی که در راستای ساخت و
  استقرار نرم‌افزار به شیوه‌ی ایمن کمک می‌کند.

**احرازهویت متوالی:**
  وقتی داده‌های احرازهویت در صفحات متوالی درخواست 
  می‌شود به جای اینکه یکبار بر روی صفحه‌ای واحد درخواست گردد.

**مدیریت نشست:** مجموعه‌ای از کنترل‌ها که کمک می‌کند
  برنامه‌های کاربردی وب نشست‌های 
  http
  را به شیوه‌ای امن مدیریت کند.

  مقادیر و شناسه‌های نشست نباید در آدرس صفحات، خطاها
  و یا رویداد‌ها افشاء گردد. این شناسه‌ها تنها می‌بایست در سرآیند کوکی
  قرار گیرد. به عنوان مثال شناسه‌های مربوط به نشست را
  تحت قالب پارامتر‌های درخواست
  GET
  ارسال نکنید.

**داده‌های وضعیت:** داده‌هایی که توسط برنامه‌کاربردی و یا سرور
  مورد استفاده قرار می‌گیرند تا ارتباط پایدار کاربر را میسر کنند و
  وضعیت کاربر به صورت پیوسته در درخواست‌های متوالی باقی بماند.

**سیستم:** یک اصطلاح عمومی که سیستم‌عامل‌ها، وب‌سرور، فریم‌ورک‌های کاربردی
  و زیرساخت‌های مرتبط را پوشش می‌دهد.

**تنظیمات سیستم:** مجموعه‌ای از کنترل‌ها که اطمینان می‌دهد
  اجزاء زیرساختی نرم‌افزار به صورت ایمن استقرار یافته است.

**عامل تهدید:** هر چیزی که ممکن است تاثیر منفی بر سیستم داشته باشد.
  این ممکن است یک کاربر مخرب باشد که می‌خواهد کنترل‌های امنیتی سیستم را
  به خطر بیندازد، ممکن است یک سوء استفاده تصادفی از سیستم باشد یا
  یک تهدید فیزیکی مانند آتش‌سوزی یا سیل باشد.

**مرز‌های اعتماد:** یک مرز اعتماد، اجزای سیستم را
  تحت کنترل مستقیم شما قرار می‌دهد. تمامی اتصالات و داده‌های سیستم‌های خارج
  از کنترل مستقیم شما، از جمله کلیه کاربران و سیستم‌هایی که توسط طرف‌های دیگر
  مدیریت می‌شوند، باید غیرقابل اعتماد در نظر گرفته شوند و قبل از مجازشماری برای
  هرگونه تعامل با سیستم شما می‌بایست بررسی و تایید شوند.

**آسیب‌پذیری:** ضعفی که سیستم را مستعد حمله یا آسیب می‌کند.

\newpage
