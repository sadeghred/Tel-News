# معماری

## هدف معماری

Tel-News دریافت Source، درک خبر، آماده‌سازی تحریریه‌ای، دسته‌بندی و انتشار مقصد را به Stageهای مستقل تقسیم می‌کند.

```text
Sources
  ↓
Source Adapters
  ↓
Normalization / Transcript
  ↓
Event & Relevance Processing
  ↓
Clustering / Deduplication
  ↓
Category Classification
  ↓
Writing / Quality / Metadata
  ↓
Review / Routing
  ↓
Platform Output Adapters
```

## لایه Source

Collectorهای اختصاصی، Telegram، Website، محتوای YouTube و Adapterهای آینده را مدیریت می‌کنند. هدف این است که ورودی‌های ناهمگون قبل از Pipeline مشترک Normalize شوند.

## لایه Processing

Pipeline تا جای ممکن پردازش Deterministic محلی را انجام می‌دهد و Taskهای Semantic منتخب را به AI-Hub می‌سپارد.

## لایه Classification

دسته‌بندی یک Stage اصلی معماری است. هر خبر می‌تواند به دسته‌ای مانند ورزشی، سیاسی، عمومی یا Category سفارشی آینده تخصیص داده شود.

## لایه Routing

Category و Destination دو مفهوم مستقل هستند. Ruleهای Routing می‌توانند هر دسته را به Channel یا Platform متفاوت بفرستند.

## لایه Output

Output Adapterها رفتار اختصاصی هر Platform را از موتور اصلی خبر جدا می‌کنند. Telegram یکی از Implementationهاست و معماری برای Destinationهای بیشتر طراحی شده است.

## Administration

ابزارهای Admin وضعیت Source، Categoryها، Monitoring، Reporting، تنظیمات انتشار و وضعیت عملیاتی را مدیریت می‌کنند، بدون اینکه Core Pipeline را به یک پلتفرم خاص محدود کنند.
