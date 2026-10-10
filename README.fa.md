# Tel-News

**سامانه هوشمند چندمنبعی جمع‌آوری، تحلیل، دسته‌بندی و انتشار چندپلتفرمی اخبار**

[English](README.md) · [معماری](docs/fa/ARCHITECTURE.md) · [Pipeline](docs/fa/PIPELINE.md) · [انتشار](docs/fa/PUBLISHING.md) · [امنیت](docs/fa/SECURITY.md)

> **Repository عمومی:** فقط برای معرفی پروژه و مستندات است. سورس خصوصی، Credentialهای Production، Database، بسته قابل Deploy و فایل دانلود برنامه منتشر نمی‌شوند.

## معرفی

Tel-News صرفاً یک «ربات تلگرام» نیست. هسته اصلی آن یک **سامانه برنامه‌پذیر پردازش و انتشار خبر** است که اخبار را از چند نوع منبع دریافت می‌کند، داده‌ها را Normalize و تحلیل می‌کند، موضوع خبر را تشخیص می‌دهد، موارد تکراری را کاهش می‌دهد، متن مناسب انتشار تولید می‌کند و هر دسته خبری را به مقصد مناسب در پلتفرم‌های مختلف هدایت می‌کند.

Telegram یکی از Sourceها، Interfaceهای مدیریتی و مقصدهای انتشار پروژه است؛ نه مرز اصلی معماری آن.

## قابلیت‌های اصلی

- دریافت خبر از چند نوع Source
- معماری Source برای Telegram، Website و YouTube
- تبدیل و Normalization ورودی‌ها به متن قابل پردازش
- تحلیل Event و Relevance با AI
- Semantic Processing و Clustering
- Deduplication پیش از انتشار
- بازنویسی و آماده‌سازی خبر فارسی
- Quality Control
- تولید Metadata و Hashtag
- نگهداری State پردازش در Database
- Admin Review و Monitoring
- **دسته‌بندی خودکار اخبار بر اساس موضوع**
- **ارسال مستقل هر دسته خبری به کانال‌ها و مقصدهای متفاوت**
- **معماری انتشار در چند پلتفرم**
- اتصال مرکزی به AI-Hub

## ایده اصلی: یک‌بار دسته‌بندی، انتشار در هر مقصد

یکی از مهم‌ترین اهداف معماری این است که تشخیص **«این خبر درباره چیست؟»** از تصمیم **«این خبر کجا منتشر شود؟»** جدا باشد.

```text
News Sources
     ↓
Ingestion / Normalization
     ↓
Event + Relevance Analysis
     ↓
Clustering / Deduplication
     ↓
News Classification
     ├── ورزشی
     ├── سیاسی
     ├── عمومی
     └── دسته‌های قابل تنظیم دیگر
     ↓
Writing / Quality / Metadata
     ↓
Destination Routing
     ├── کانال‌های تخصصی Telegram
     ├── سایر پیام‌رسان‌ها / پلتفرم‌ها
     └── مقصدهای انتشار آینده
```

در نتیجه یک موتور پردازش مرکزی می‌تواند همزمان چند کانال موضوعی و چند پلتفرم انتشار را تغذیه کند، بدون اینکه برای هر مقصد کل Pipeline دوباره ساخته شود.

## منابع خبری

معماری برای Sourceهای ناهمگون طراحی شده است:

- کانال‌های Telegram
- Websiteها
- YouTube و محتوای متنی استخراج‌شده از ویدئو
- Adapterهای قابل توسعه برای Sourceهای آینده

ورودی هر Source قبل از ورود به Pipeline مشترک Normalize می‌شود.

## معماری AI

Tel-News به **AI-Hub** مرکزی متصل است و لازم نیست منطق هر AI Provider داخل خود سامانه خبری Hard-code شود. Stageهای AI بسته به Configuration می‌توانند شامل event extraction، relevance filtering، semantic processing، translation، rewriting و quality review باشند.

## نقش Telegram

Telegram بخش مهمی از پروژه است و برای Source monitoring، مدیریت دسته‌ها/کانال‌ها، کنترل‌های Admin، گزارش‌ها، پیام‌های کاربران و انتشار در مقصدهای Telegram استفاده می‌شود.

اما محصول اصلی، **سامانه پردازش، دسته‌بندی و انتشار چندپلتفرمی اخبار** است.

## قابلیت‌های عملیاتی فعلی

معماری Admin شامل مدیریت مستقل Sourceهای خبری، Categoryها، قابلیت‌های مرتبط با تبلیغات، گزارش‌گیری، پیام‌های کاربران و وضعیت کلی سیستم است. مدیریت Sourceهای Telegram مبتنی بر Database است و فعال/غیرفعال‌کردن و Configuration مستقل هر Source را پشتیبانی می‌کند.

## امنیت

Repository عمومی شامل API Key، Credential تلگرام، Secretهای AI Provider، آدرس خصوصی سرور، Database Production، Secretهای Authentication، Log خصوصی یا سورس قابل Deploy نیست.

## وضعیت پروژه

Tel-News پروژه‌ای فعال و در حال توسعه است. Ingestion، Processing، AI Integration، Administration و Publishing به‌صورت مرحله‌ای توسعه پیدا می‌کنند و اجزای عملیاتی موجود حفظ می‌شوند.

## تماس

- تلگرام: [@Sadeghred](https://t.me/Sadeghred)
- ایمیل: [sadeghred@gmail.com](mailto:sadeghred@gmail.com)

---
© 2026 Tel-News Project
