# Pipeline پردازش خبر

مدل پردازش به Stageهای مستقل تقسیم شده تا هر مسئولیت جداگانه قابل Test، جایگزینی و بهبود باشد.

## Stageهای مفهومی

1. **Source ingestion** — دریافت محتوا از Sourceهای تنظیم‌شده
2. **Normalization / transcript** — تبدیل ورودی‌های مختلف به متن و Metadata قابل پردازش
3. **Event extraction** — تشخیص رویداد اصلی خبر
4. **Relevance analysis** — حذف محتوای خارج از معیارهای تحریریه
5. **Clustering / deduplication** — تشخیص گزارش‌های هم‌پوشان و رویدادهای تکراری
6. **Classification** — تعیین دسته مناسب خبر
7. **Writing / rewriting** — تولید متن فارسی مناسب انتشار در صورت نیاز
8. **Quality control** — کنترل خروجی پیش از انتشار
9. **Metadata / hashtags** — افزودن Metadata انتشار
10. **Review / routing** — تعیین مقصد بر اساس Category و Configuration
11. **Publishing** — ارسال از طریق Adapter پلتفرم مناسب

## AI-Hub

Stageهای AI منتخب از Task layer مرکزی AI-Hub استفاده می‌کنند. در نتیجه Provider/Model و Credential از Core پروژه Tel-News جدا می‌مانند.

## پردازش Local-First

عملیاتی که نیاز به Generative AI ندارند می‌توانند Local باقی بمانند تا Callهای غیرضروری AI کاهش پیدا کند و Pipeline کارآمدتر و Deterministicتر باشد.
