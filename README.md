# UT Brawlforge

## ساختار پروژه

در زیر ساختار فایل‌ها و پوشه‌های اصلی پروژه به همراه توضیح مختصری از هرکدام آورده شده است:

```
.
├── config.py        # تنظیمات و پیکربندی‌های اصلی بازی (مانند ابعاد صفحه، سرعت و ...)
├── .git             # پوشه مربوط به سیستم کنترل نسخه گیت (نادیده گرفته شود)
├── .gitignore       # لیستی از فایل‌ها و پوشه‌هایی که توسط گیت نادیده گرفته می‌شوند
├── README.md        # همین فایلی که در حال مطالعه آن هستید، راهنمای پروژه
├── requirements.txt # لیست کتابخانه‌ها و وابستگی‌های لازم برای اجرای پروژه
├── run_game.py      # اسکریپت اصلی برای اجرای بازی
└── src              # پوشه اصلی کدهای منبع بازی
    ├── assets       # شامل فایل‌های جانبی بازی مانند تصاویر و صداها
    │   ├── images   # پوشه تصاویر استفاده شده در بازی
    │   │   └── .gitkeep # یک فایل خالی برای حفظ پوشه در گیت
    │   └── sounds   # پوشه صداهای استفاده شده در بازی
    │       └── .gitkeep # یک فایل خالی برای حفظ پوشه در گیت
    ├── engine       # شامل منطق اصلی و موتور بازی
    │   ├── game.py  # کلاس‌ها و توابع اصلی مربوط به گیم‌پلی و مدیریت بازی
    │   └── __init__.py # فایل مورد نیاز پایتون برای شناسایی این پوشه به عنوان یک پکیج
    └── utils.py     # شامل توابع کمکی و ابزارهای عمومی مورد استفاده در پروژه
```

## توضیحات فایل‌ها و پوشه‌ها

*   `config.py`: این فایل شامل تنظیمات کلی بازی مانند ابعاد پنجره، رنگ‌ها، سرعت فریم و سایر مقادیر ثابت است.
*   `.gitignore`: این فایل به گیت می‌گوید که کدام فایل‌ها و پوشه‌ها را نباید در مخزن (repository) ذخیره کند. معمولاً فایل‌های موقت، کش‌ها و پوشه‌های مربوط به محیط مجازی در این لیست قرار می‌گیرد. (لازم به کاری از طرف شما نیست.)
*   `README.md`: این فایل راهنمای پروژه است و اطلاعاتی در مورد پروژه، نحوه نصب و اجرا و ساختار آن ارائه می‌دهد.
*   `requirements.txt`: این فایل لیست تمام کتابخانه‌های خارجی که پروژه شما به آن‌ها نیاز دارد را مشخص می‌کند. با استفاده از این فایل می‌توان به راحتی وابستگی‌های پروژه را نصب کرد. (اگر پکیج یا کتابخانه‌ای استفاده می‌کنید، باید آن را با ورژن در این فایل ذکر کنید.)
*   `run_game.py`: این اسکریپت نقطه ورود اصلی برای اجرای بازی است. با اجرای این فایل، بازی شروع می‌شود.
*   `src/`: این پوشه حاوی تمام کدهای منبع اصلی بازی است.
    *   `src/assets/`: این پوشه برای نگهداری فایل‌های تصویری، صوتی و سایر منابع مورد نیاز بازی استفاده می‌شود.
        *   `src/assets/images/`: مخصوص نگهداری تصاویر بازی.
        *   `src/assets/sounds/`: مخصوص نگهداری فایل‌های صوتی بازی.
    *   `src/engine/`: این پوشه شامل منطق اصلی و مرکزی بازی است.
        *   `src/engine/game.py`: این فایل احتمالاً شامل کلاس اصلی بازی، مدیریت حلقه بازی (game loop)، پردازش رویدادها و سایر بخش‌های کلیدی گیم‌پلی است.
    *   `src/utils.py`: این فایل شامل توابع و کلاس‌های کمکی است که در بخش‌های مختلف پروژه مورد استفاده قرار می‌گیرند تا از تکرار کد جلوگیری شود و خوانایی کد افزایش یابد.

## نحوه نصب و اجرا

برای نصب و اجرای این پروژه، مراحل زیر را دنبال کنید:

1.  **نصب dependencyها:**

    کتابخانه‌های مورد نیاز پروژه را با استفاده از فایل `requirements.txt` نصب کنید:
    ```bash
    pip install -r requirements.txt
    ```

2.  **اجرای بازی: باید پیاده‌سازی شود**

    بازی را با اجرای اسکریپت `run_game.py` شروع کنید:
    ```bash
    python run_game.py
    ```