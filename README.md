# CompanyManagement

#### از شما خواسته شده مدیریت کارکنان یک شرکت را در اختیار بگیرید.

با تمرکز بر مفاهیم **وراثت** (Inheritance) و **کالکشن‌ها** (Collections)، کلاس‌های موردنیاز را مطابق توضیحات زیر پیاده‌سازی کنید:

## Staff

یک کلاس پایه برای تمام کارکنان شرکت.

دارای فیلدهای زیر:

* `String firstName` نام کارمند
* `String lastName` نام خانوادگی کارمند
* `int workExperience` سابقه کاری کارمند
* `boolean committedCrime` وضعیت تخلف یا جرم کارمند
* `double baseSalary` حقوق پایه کارمند

### متد 

* Getter و Setter برای تمامی فیلدها


---

## Employee

کارمند، نوعی Staff است.

این کلاس به عنوان کلاس والد برای:

* Salesman
* Accountant

استفاده می‌شود.

### متدهایی که باید پیاده‌سازی کنید

1. `public double  countBonus()`

محاسبه bonus برای کارمندان است که با فرمول زیر محاسبه میشود:
```text
workExperience × 5 

```
---

## Salesman

فروشنده، نوعی Employee است.

## متد ها
* `double countSalary()`

حقوق فروشنده به صورت زیر محاسبه می‌شود:

```text
baseSalary + (workExperience × 60) + bonus
```

برای این کلاس متدهای `equals()` و `hashCode()` نیز پیاده‌سازی شوند.

---

## Accountant

حسابدار، نوعی Employee است.


## متد ها
* `double countSalary()`
حقوق حسابدار به صورت زیر محاسبه می‌شود:

```text
baseSalary + (workExperience × 50) + bonus
```

برای این کلاس متدهای `equals()` و `hashCode()` نیز پیاده‌سازی شوند.

---



## Manager

مدیر، نوعی Staff است.

دارای فیلدهای زیر:

* `ArrayList<Salesman> salesmen`
* `ArrayList<Accountant> accountants`




**حتماً از قواعد کپسول‌سازی استفاده کنید و از لیست‌ها در Getterها محافظت کنید.**

---

### متدهایی که باید پیاده‌سازی کنید

1. `boolean addSalesman(Salesman salesman)`

اضافه کردن یک فروشنده به لیست فروشندگان.

* اگر ورودی `null` باشد عملیات ناموفق است.
* در غیر این صورت فروشنده به لیست اضافه شده و `true` برگردانده می‌شود.

---

2. `boolean addAccountant(Accountant accountant)`

اضافه کردن یک حسابدار به لیست حسابداران.

* اگر ورودی `null` باشد عملیات ناموفق است.
* در غیر این صورت حسابدار به لیست اضافه شده و `true` برگردانده می‌شود.

---



3. `boolean fireSalesman(String firstName)`

اخراج یک فروشنده با نام مشخص.

* فروشنده باید در لیست وجود داشته باشد.
* مقدار `committedCrime` باید برابر `true` باشد.
* در صورت موفقیت فروشنده از لیست حذف شده و `true` برگردانده می‌شود.
* در غیر این صورت `false` برگردانده می‌شود.

---

4. `boolean fireAccountant(String firstName)`

اخراج یک حسابدار با نام مشخص.

* حسابدار باید در لیست وجود داشته باشد.
* مقدار `committedCrime` باید برابر `true` باشد.
* در صورت موفقیت حسابدار از لیست حذف شده و `true` برگردانده می‌شود.
* در غیر این صورت `false` برگردانده می‌شود.

---



5. `List<Salesman> getSalesmen()`

برگرداندن لیست فروشندگان.

---

6. `List<Accountant> getAccountants()`

برگرداندن لیست حسابداران.


---

7. `int getTotalAvailable()`

تعداد کل کارکنان موجود در شرکت را برگرداند.

```text
salesmen.size() +
accountants.size() +
```
---

* `double countSalary()`
محاسبه حقوق مدیر با فرمول زیر:

```text
baseSalary + (workExperience × 70)
```
