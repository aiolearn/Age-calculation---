<h1 align="center">Welcome to Age calculation Project! 👋</h1>

# Age Calculation Project!

This project is for calculating age from year to month, week, minute and second.That is, you give the program your age in years, for example 25 years, and the program converts your age into months, weeks, days, etc.


## Modules
We use time and calendar.isleap modules
```python
import time
from calendar import isleap
```

We use modules to solve the program faster and optimize the codes. Our suggestion is to use the modules and get used to them

## Usage
First, we need to find out whether it is a leap year or not
```python
def judge_leap_year(year):
    if isleap(year):
        return True
    else:
        return False
```

The next step is to convert to month, day, hour, minute and second
 ```python
def month_days(month, leap_year):
    if month in [1, 3, 5, 7, 8, 10, 12]:
        return 31
    elif month in [4, 6, 9, 11]:
        return 30
    elif month == 2 and leap_year:
        return 29
    elif month == 2 and (not leap_year):
        return 28

def to_hours(days):
    hours = days * 24
    return hours

def to_seconds(days):
    seconds = days * 24 * 3600
    return seconds
```
The next step is to get the user's age and convert it to the requested values, for example 25 years
```python
year = int(age)
month = year * 12 + localtime.tm_mon
day = 0
```

Calculate the number of days using the judge_leap_year function
```python
begin_year = int(localtime.tm_year) - year
end_year = begin_year + year

for y in range(begin_year, end_year):
    if (judge_leap_year(y)):
        day = day + 366
    else:
        day = day + 365
```

Checking if it is a leap year or not
```python
leap_year = judge_leap_year(localtime.tm_year)

for m in range(1, localtime.tm_mon):
    day = day + month_days(m, leap_year)

day = day + localtime.tm_mday
```

Convert days to hours and minutes

```python
hours = to_hours(day)
seconds = to_seconds(day)
```

And finally we display the result

```python
print("age is %d years or " % (year), end="")
print("%d months or %d days" % (month, day), end="")
print(" or %d hours or %d seconds" % (hours, seconds))
```
result = age is 16 years or 194 months or 5901 days or 141624 hours or 509846400 seconds!

## Result

This project was written by Majid Tajanjari and the Aiolearn team, and we need your support!❤️

# پروژه محاسبه سن!
این پروژه برای محاسبه سن سال به ماه، هفته، دقیقه و ثانیه است. یعنی شما سن خود را به سال مثلا 25 سال به برنامه می دهید و برنامه سن شما را به ماه، هفته، روز و ... تبدیل می کند.


## Modules
ما از ماژول های time و calendar.isleap استفاده می کنیم
```python
import time
from calendar import isleap
```

ما از ماژول ها برای حل سریعتر برنامه و بهینه سازی کدها استفاده می کنیم. پیشنهاد ما این است که از ماژول ها استفاده کنید و به آنها عادت کنید

## Usage
ابتدا باید بررسی کنیم که آیا سال کبیسه است یا خیر
```python
def judge_leap_year(year):
    if isleap(year):
        return True
    else:
        return False
```
مرحله بعدی تبدیل به ماه، روز، ساعت، دقیقه و ثانیه است

 ```python
def month_days(month, leap_year):
    if month in [1, 3, 5, 7, 8, 10, 12]:
        return 31
    elif month in [4, 6, 9, 11]:
        return 30
    elif month == 2 and leap_year:
        return 29
    elif month == 2 and (not leap_year):
        return 28

def to_hours(days):
    hours = days * 24
    return hours

def to_seconds(days):
    seconds = days * 24 * 3600
    return seconds
```
مرحله بعدی دریافت سن کاربر و تبدیل آن به مقادیر درخواستی مثلا 25 سال است
```python
year = int(age)
month = year * 12 + localtime.tm_mon
day = 0
```
تعداد روزها را با استفاده از تابع judge_leap_year محاسبه کنید
```python
begin_year = int(localtime.tm_year) - year
end_year = begin_year + year

for y in range(begin_year, end_year):
    if (judge_leap_year(y)):
        day = day + 366
    else:
        day = day + 365
```

بررسی اینکه آیا سال کبیسه است یا خیر
```python
leap_year = judge_leap_year(localtime.tm_year)

for m in range(1, localtime.tm_mon):
    day = day + month_days(m, leap_year)

day = day + localtime.tm_mday
```

تبدیل روز به ساعت و دقیقه

```python
hours = to_hours(day)
seconds = to_seconds(day)
```

و در نهایت نتیجه را نمایش می دهیم

```python
print("age is %d years or " % (year), end="")
print("%d months or %d days" % (month, day), end="")
print(" or %d hours or %d seconds" % (hours, seconds))
```
نتیجه = سن 16 سال یا 194 ماه یا 5901 روز یا 141624 ساعت یا 509846400 ثانیه است!

## Result

این پروژه توسط مجید تجنجری و تیم Aiolearn نوشته شده است و ما به حمایت شما نیازمندیم!❤️