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

## part4: Dashboards
### First dashboard: quantity of orders by branch over time(yearly)
In this dashboard, there are two graphs, one shows the total number of orders to Tekfik provinces and the other shows the trend of the same over time.
The reason for the significant difference in the numbers related to the last year and the first year is the incompleteness of the data.


![001](https://github.com/Mahdi-mghs/Retrieve_Market/assets/77622627/2acb549c-5b91-45aa-8305-27a44e1eb9c7)

### Second dashboard: Discount effect
This dashboard contains two graphs, in the graph on the left is the average number of orders in terms of the discount percentage, which is displayed in several sections according to the type of laptop. It can be seen that the amount of discount did not have a significant impact on sales, except for the type of Net laptops. Book, which has a little effect of the discount on this type of laptop.
The chart on the right is similar to the chart on the left, but this time the dollar profit of different types of laptops has been compared
![002](https://github.com/Mahdi-mghs/Retrieve_Market/assets/77622627/d5607086-f352-4953-a340-5fcf9be2357f)

### The third dashboard: the amount of sales by category and manufacturing company
In this dashboard, you can see the amount of sales or profit in terms of dollars and tomans by the type of laptop and manufacturing companies using the created slicer. In addition, on the right side, you can see this comparison based on the number of sales.
As it is known, netbook laptop type and Dell company have a high share in this store
![003](https://github.com/Mahdi-mghs/Retrieve_Market/assets/77622627/a55c62cc-a56a-49ab-aa4b-5b39b9517f51)
### The fourth dashboard: sales comparison by months of the year
In this dashboard, you can compare the amount of sales and profit (number, sales in terms of dollars and Tomans) according to the months of the year, and it can be seen that the amount of sales decreases in October and November, which leads to the New Year.
![004](https://github.com/Mahdi-mghs/Retrieve_Market/assets/77622627/efe1480a-d785-4e71-bede-5f92ce5a6b1a)


#### The fifth dashboard: comparison based on order type and delivery time

In this data, the orders are divided into 4 parts according to the delivery time, which can be seen in this dashboard that the orders that arrive later include the amount of profit and more orders.
It can be seen in the graph on the left that there is no difference between the types of orders in their average prices in each category.

![005](https://github.com/Mahdi-mghs/Retrieve_Market/assets/77622627/90927487-18f8-4e7d-a2a8-947ec62ee6ce)
### The sixth dashboard: profit and sales (number, dollars and tomans) by city over time
As it is known, Isfahan, Tehran and Mashhad have the largest share
![006](https://github.com/Mahdi-mghs/Retrieve_Market/assets/77622627/1322871d-d751-475d-b073-2741afc1ae5b)

### The seventh dashboard: the amount of sales by province during different years
![007](https://github.com/Mahdi-mghs/Retrieve_Market/assets/77622627/3ac0a2ce-13c2-48c7-979c-3a4b8ed45a7a)

### Eighth dashboard: Statistics of the current month, season and year
In this section, the amount of your sales will be emailed to specific people using the PowerBA server
![008](https://github.com/Mahdi-mghs/Retrieve_Market/assets/77622627/e79f4b9b-2ad8-4413-a925-a353196c8539)
### Ninth dashboard: types of sales parameters by company during the year
![009](https://github.com/Mahdi-mghs/Retrieve_Market/assets/77622627/e8cb1e72-d8d2-4760-8fbc-7028b4b23ea4)
### 10th Dashboard: Comparison of various sales and profit parameters for different years during the month
![010](https://github.com/Mahdi-mghs/Retrieve_Market/assets/77622627/ea6583d2-63cb-4fb5-a1b3-22ad3371af24)
### The 11th dashboard: displaying all kinds of simultaneous sales parameters by company and laptop type during the year
![011](https://github.com/Mahdi-mghs/Retrieve_Market/assets/77622627/1361ffd8-8b87-4da9-94e6-fe220f729782)
### The twelfth dashboard: the trend of the company's total sales during the year
As it can be seen, the company's dollar sales have been stable during these years and there has been no progress.
The exchange rate of Tomani and Rial cannot be a good criterion due to the high inflation in Iran
![012](https://github.com/Mahdi-mghs/Retrieve_Market/assets/77622627/11f61c02-5a3f-4e81-aebd-6d57fbe3b883)
### The 13th dashboard: the amount of sales of laptops by tags, type of RAM and the number of companies and factories related to each type of RAM and type of laptop
![013](https://github.com/Mahdi-mghs/Retrieve_Market/assets/77622627/933cfa6c-b40b-4254-8adf-0116dca67c43)
### 14th dashboard: The impact of dollar growth on sales and profits
![014](https://github.com/Mahdi-mghs/Retrieve_Market/assets/77622627/adddc651-7fef-411f-b46e-11b8e7ce0903)
### Dashboard 15M: here is the result of the investigation of the relationship between the price and weight of laptops in python
As it is known, there is no special correlation
![015](https://github.com/Mahdi-mghs/Retrieve_Market/assets/77622627/1c2eeaf9-111c-4fcb-a57b-ed02ef0ff62b)
### Dashboard 16M: Review of CPU brands in Python
As it is known, most of the laptops in the CPU store are related to Intel, and the average prices of related laptops are also higher.
![016](https://github.com/Mahdi-mghs/Retrieve_Market/assets/77622627/c2127afb-305c-4b46-8646-39d311751412)
### Dashoboard 17: Comparison of laptop demand by CPU brand over the years in python
![017](https://github.com/Mahdi-mghs/Retrieve_Market/assets/77622627/35fb6e35-78e9-43f0-8200-8add76b9cf44)







[**Torob**](https://torob.com/browse/99/%D9%84%D9%BE-%D8%AA%D8%A7%D9%BE-%D9%88-%D9%86%D9%88%D8%AA-%D8%A8%D9%88%DA%A9-laptop/) is a Comprehensive website, because it has a big Variety laptops and prices from all market, so it's best target to _Crawling_

website use *api structures*, so need a little more time for crawling currectly and also our raw data need a huge cleaning
> some datas are not in right position, first we should with text scraping method replace them by correct value, you can check [torob_cleaning](https://github.com/Mahdi-mghs/Retrieve_Market/blob/main/Crawl/torob_cleaning.ipynb) for more details
