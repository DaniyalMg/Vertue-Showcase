# 🎮 Vertue Site | پلتفرم خرید طلا و سکه در متاورس

[![Python](https://img.shields.io/badge/Python-3.9%2B-blue?style=for-the-badge&logo=python)](https://www.python.org/)
[![Django](https://img.shields.io/badge/Django-4.x-green?style=for-the-badge&logo=django)](https://www.djangoproject.com/)
[![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white)](https://getbootstrap.com/)
[![PostgreSQL](https://img.shields.io/badge/Database-PostgreSQL-lightgrey?style=for-the-badge&logo=postgresql)](https://www.postgresql.org/)

**Vertue Site** یک پلتفرم تخصصی برای خرید و فروش طلای مجازی (In-Game Currency) در محیط‌های متاورسی و بازی‌های آنلاین است. این پروژه با هدف ایجاد محیطی امن، سریع و کاربرپسند برای معامله‌گران بازی طراحی شده است.

> ⚠️ **توجه:** کدهای منبع به دلیل محرمانه بودن پروژه اصلی، در اینجا موجود نیستند. این مخزن شامل مستندات فنی، معماری و دموهای وب‌سایت است.

---

## ✨ ویژگی‌های کلیدی

### 🎮 برای بازیکنان (Users)
*   **خرید آنی طلا:** فرآیند خرید ساده و سریع برای شارژ حساب بازی.
*   **داشبورد کاربری:** مشاهده تاریخچه تراکنش‌ها، موجودی فعلی و وضعیت سفارشات.
*   **بسته‌های متنوع:** انتخاب از بین بسته‌های مختلف طلایی و سکه با قیمت‌های رقابتی.
*   **پشتیبانی تیکتی:** سیستم ارسال تیکت برای رفع مشکلات پرداخت یا عدم دریافت کالا.
*   **ورود امن:** احراز هویت امن با استفاده از توکن‌های JWT یا Session.

### 👨‍💻 برای ادمین‌ها (Admin)
*   **مدیریت تراکنش‌ها:** مشاهده، تأیید و لغو سفارشات خرید طلا.
*   **مدیریت کاربران:** نظارت بر کاربران فعال، مسدود کردن حساب‌های متخلف.
*   **مدیریت محصولات:** افزودن، ویرایش و حذف بسته‌های طلایی و تعیین قیمت‌ها.
*   **گزارش‌گیری مالی:** مشاهده درآمد روزانه، هفتگی و ماهانه سایت.

---

## 🛠️ تکنولوژی‌ها و معماری

این پروژه با استفاده از فریم‌ورک قدرتمند **Django** و رعایت اصول **Clean Architecture** توسعه یافته است:

| لایه | تکنولوژی‌ها | توضیحات |
| :--- | :--- | :--- |
| **Backend** | Python, Django, Django REST Framework (DRF) | پیاده‌سازی بک‌اند و APIها |
| **Database** | PostgreSQL, Django ORM | ذخیره‌سازی امن داده‌های مالی و کاربری |
| **Frontend** | HTML5, CSS3, JavaScript, Tailwind CSS | طراحی رابط کاربری مدرن و واکنش‌گرا |
| **Security** | CSRF Protection, XSS Prevention | محافظت از تراکنش‌های مالی |
| **Deployment** | Docker, Nginx, Gunicorn | استقرار در سرورهای لینوکسی |

---

## 📸 دمو و اسکرین‌شات‌ها

### 1. صفحه اصلی و لیست بسته‌ها
نمایش بسته‌های طلایی با طراحی جذاب و گیمینگ.
![صفحه اصلی](https://via.placeholder.com/800x400?text=Game+Store+Home+Page)
*(اسکرین‌شات از صفحه اصلی سایت را اینجا بگذارید)*

### 2. فرآیند خرید (Checkout)
صفحه نهایی پرداخت و تأیید سفارش.
![فرآیند خرید](https://via.placeholder.com/800x400?text=Checkout+Page+Demo)
*(اسکرین‌شات از صفحه پرداخت را اینجا بگذارید)*

### 3. داشبورد کاربری
مشاهده تاریخچه خریدها و موجودی.
![داشبورد کاربری](https://via.placeholder.com/800x400?text=User+Dashboard+Demo)
*(اسکرین‌شات از داشبورد کاربر را اینجا بگذارید)*

### 4. پنل مدیریت
مدیریت سفارشات و کاربران.
![پنل مدیریت](https://via.placeholder.com/800x400?text=Admin+Panel+Demo)
*(اسکرین‌شات از پنل ادمین را اینجا بگذارید)*

---

## 🏗️ ساختار پروژه (High-Level Architecture)

ساختار پروژه به صورت ماژولار و استاندارد دجنو طراحی شده است:

```text
Vertue-Site/
├── core/                 # تنظیمات اصلی پروژه (Settings, URLs)
├── store/                # اپلیکیشن اصلی فروشگاه
│   ├── models.py         # مدل‌های Product, Order, Transaction, User
│   ├── views.py          # ویوهای صفحه اصلی، خرید، سبد خرید
│   ├── templates/        # قالب‌های HTML
│   └── static/           # فایل‌های استاتیک (CSS, JS)
├── accounts/             # اپلیکیشن مدیریت کاربران
├── admin_panel/          # پنل مدیریت سفارشی‌سازی شده
├── requirements.txt      # لیست وابستگی‌ها
└── Dockerfile            # فایل ساخت ایمیج داکر
