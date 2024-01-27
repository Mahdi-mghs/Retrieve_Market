# Retrieve_Market

### What is target & story ?

> این پروژه درباره اطلاعات شرکت (فرضی) لوتک است. شرکتی که در زمینه فروش لپ تاپ فعالیت دارد. این شرکت از زمان شروع کار خود تمامی اطلاعات فروش خود را در فایل های csv ذخیره کرده است، به همین علت (عدم طراحی درست ذخیره سازی اطلاعات) به مشکلات جدی در کسب و کار خود برخورد کرده و تا مرز برشکستی نیز پیش رفته است و چندین سال نیز مجبور به تعطیلی شده است.
حال با تغییر مدیریت، این شرکت به فکر بازسازی مجدد خود و در دست گرفتن بازار فروش لپ تاپ است. مدیر جدید که بسیار خوش فکر و آینده نگر است برای خارج شدن از این بحران تصمیم به استخدام افرادی توانا در زمینه ذخیره سازی و تحلیل داده گرفته است. برای همین او آگهی شغلی را منتشر کرده است و به عنوان بخش فنی فرآیند استخدام قسمتی از داده‌های فروش گذشته خود را در اختیار کارجویان قرار داده است. و از آن ها می خواهد تا نیازهای لازم برای شرکت را بر روی این داده ها انجام دهند. او قصد دارد در انتها بهترین افراد را در این زمینه به استخدام شرکت درآورد.

## Part 1: Database Design

![drawSQL-laptop-store-export-2024-01-22](https://github.com/Mahdi-mghs/Retrieve_Market/assets/47474659/136b983b-c7ad-496e-b993-68da097f0932)

As you see we have __laptops__ as a main table and tried to support all queries needed, you can check [connect_sql](https://github.com/Mahdi-mghs/Retrieve_Market/blob/main/BI/connect_sql.ipynb) for more details 🦖

## Part 2: DataWare House Design

![image](https://github.com/Mahdi-mghs/Retrieve_Market/assets/47474659/29c9c1bf-8ff5-4622-9bb7-15de2a08e58c)

Trying to create **Star** design for have a good optimiztion

Also we additionally add USD_Toman_History for Taking the fluctuations of the country's currency in consecutive years, it would be so functionall in futuer laptops price

## Part 3: Competing company

We have many comptetitor ! for overcoming them we need to recogonize and getting their datas for compare our data

[**Torob**](https://torob.com/browse/99/%D9%84%D9%BE-%D8%AA%D8%A7%D9%BE-%D9%88-%D9%86%D9%88%D8%AA-%D8%A8%D9%88%DA%A9-laptop/) is a Comprehensive website, because it has a big Variety laptops and prices from all market, so it's best target to _Crawling_

website use *api structures*, so need a little more time for crawling currectly and also our raw data need a huge cleaning (some datas are not in right position, first we should with text scraping method replace them by correct value)
