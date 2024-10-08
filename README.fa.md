[![en](https://img.shields.io/badge/lang-eng-red.svg)](https://github.com/arzhangap/compose-persian-date-picker/blob/master/README.md)  
# انتخاب تاریخ کامپوز

کتابخانه آماده برای انتخاب تاریخ شمسی برای پلتفرم اندروید.

<img src="https://github.com/user-attachments/assets/e7fcb14b-a40b-46b5-98cb-69921f16967e" alt="Alt Text" width="350" />

## فهرست بارگان
1. [ویژگی‌ها](#ویژگیها)
2. [نصب](#نصب)
3. [استفاده](#استفاده)
4. [سفارشی‌سازی](#سفارشی‌سازی)
5. [حمایت](#حمایت)
6. [مشارکت](#مشارکت)
7. [مجوز](#مجوز)

---

## ویژگی‌ها

- قابلیت انتخاب تاریخ
- قابلیت اسکرول بین ماه‌ها و سال‌ها
- پشتیبانی از Material you
- قابلیت شخصی سازی

---

## نصب
در فایل `settings.gradle.kts` کد زیر را اضافه کنید:
```kts
dependencyResolutionManagement {
    repositoriesMode.set(RepositoriesMode.FAIL_ON_PROJECT_REPOS)
    repositories {
        // following line | خط زیر
        maven { url =  uri("https://jitpack.io") }
    }
}
```

سپس در فایل `build.gradle` سطح اپ (app-level) کد زیر را اضافه کنید:

```kts
    dependencies {
            // following line | خط زیر
            implementation("com.github.arzhangap:compose-persian-date-picker:1.0.0")
    } 
```


## استفاده 

```kotlin
   // State | وضعیت تاریخ‌گیر را با کد زیر دنبال کنید.
   val datePickerState = rememberPersianDatePickerState()

   // Consume | وضعیت را به کامپوزبل ارائه کنید
   PersianDatePicker(persianDatePickerState = datePickerState)

  // Open/Close Dialog | با استفاده از این تابع صفحه را باز کنید یا ببندید
  Button(onClick = { datePickerState.toggleDialog()}) {
        Text(text = "Open")
  }
    // تاریخ انتخاب شده توسط کاربر را با متغیر زیر دنبال کنید
    // در صورت انتخاب نکردن تاریخ null
    // برای گرفتن متن فرمت شده از تابع 
    // string
    // استفاده کنید
    // در صورت انتخاب نشدن تاریخ متن پیش فرض نمایش داده می شود
    // متن پیش فرض را می‌توانید در پارامتر تابع تغییر دهید
// Get formatted String
   Text(text = calenderState.chosenDate.string())
```

## حمایت

برای حمایت از این پروژه ستاره⭐ رو بزن.

<a href="https://www.coffeebede.com/arzhangap">
    <img class="img-fluid" src="https://coffeebede.ir/DashboardTemplateV2/app-assets/images/banner/default-yellow.svg" width="300" />
</a>

## مشارکت
1. ریپازتوری را Fork کنید.
2. ریپازیتوری را در سیستم خود clone کنید.
``` bash
git clone https://github.com/YOUR-USERNAME/compose-persian-date-picker.git
```
3. یک Branch برای راه حل ها و قابلیت های جدیدی که قصد ساخت آن را دارید بسازید.
``` bash
git checkout -b feature/your-feature-name
```
4. تغیرات خود را ایجاد کنید.
5. با تست کردن کد مطمئن شوید که قابلیت های جدید باعث ایجاد باگ نمی شود.
6. تغیرات را commit کنید
```bash
git commit -m "Add feature: detailed description of changes"
```
7. تغیرات را push کنید
```bash
git push origin feature/your-feature-name
```
8. یک Pull Request ایجاد کنید: به ریپازیتوری اصلی بروید و یک pull request باز کنید. توضیح دهید که چه تغیراتی ایجاد کردید و چرا.

# رهنمودهای مشارکت
- از ساختار کدهای پروژه پیروی کنید.
- تاریخچه commit ها را تمیز نگه دارید.
- هنگام افزودن ویژگی ها یا تغییر عملکرد موجود، به محدوده پروژه احترام بگذارید و قابلیت های خارج از محدوده را اضافه نکنید.
- اگر بر روی یک Bugfix یا درخواست قابلیت در بخش issues کار میکنید عدد ایراد(issue) را در PR ذکر کنید.


## مجوز
لطفا در صورت استفاده از کد(تغییر داده شده یا نشده) در پروژه خود لایسنس زیر را قرار دهید.

```
Copyright 2024 arzhangap (Arzhang Alvandi Pour)

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
```
