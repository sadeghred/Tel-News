# دسته‌بندی و انتشار چندپلتفرمی

## دسته‌بندی، بخش مرکزی سیستم است

Tel-News بر اساس Category-aware publishing طراحی شده است. Classification فقط یک Label نمایشی نیست؛ می‌تواند Routing مراحل بعدی را تعیین کند.

نمونه دسته‌ها:

- ورزشی
- سیاسی
- عمومی
- Categoryهای قابل تنظیم دیگر

## Routing از Category به Destination

هر Category می‌تواند به یک یا چند Destination متصل شود. بنابراین دسته‌های مختلف می‌توانند مستقل از هم در Channelهای تخصصی منتشر شوند.

```text
ورزشی -> مقصدهای ورزشی
سیاسی -> مقصدهای سیاسی
عمومی  -> مقصدهای عمومی
```

## طراحی Multi-Platform

Publishing پشت Output Adapterها جدا شده است. در نتیجه یک News Object پردازش‌شده می‌تواند بدون بازسازی Pipeline دریافت و تحلیل، به Platformهای مختلف ارسال شود.

Telegram در وضعیت فعلی یک Output و سطح مدیریتی مهم است، اما معماری عمداً گسترده‌تر طراحی شده تا Destinationهای پیام‌رسانی/اجتماعی دیگر نیز اضافه شوند.

## مزایا

- یک Pipeline دریافت برای چند مقصد
- Channelهای تخصصی بر اساس Category
- Core پردازش مستقل از Platform
- اضافه‌کردن آسان‌تر Outputهای جدید
- Ruleهای Classification و Quality یکسان در همه مقصدها
