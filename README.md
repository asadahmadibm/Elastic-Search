# Elastic-Search

موتور جستجوی متن باز با تجزیه و تحلیل کامل است از طریق APi میتوان داده ها را ایجاد یا جستجو و دریافت کرد

الستیک سرچ  یکی از قدرتمند‌ترین تکنولوژی‌های برنامه نویسی‌ست که در حوزه‌های مختلفی مانند دسترسی به داده‌ها و جستجوی در برنامه و جستجوی وب سایت و تحلیل حجم عظیم اطلاعات ورودی به شما کمک می‌کند. 

SQL    =>	Elastic Search Compare
----------------------------
Column   =>	Field

Row	     => Document

Table	   => Index

Schema   =>	implicit

database =>	cluster


ابزارهای مرتبط با Elasticsearch چیست؟
شرکت الاستیک چند ابزار برای راحت‌تر کار کردن با Elasticsearch توصیه کرده است که عبارتند از:

Logstash: یکی از محصولات اصلی الاستیک است که برای جمع‌آوری و پردازش داده و ارسال آن به Elasticsearch استفاده می‌شود. Logstash یک خط لوله‌ی پردازش داده‌ی مبتنی بر سرور است که این امکان را می‌دهد که داده‌ها را از منابع چندگانه به طور همزمان جذب کرده و آنها را قبل از شاخص‌گذاری در Elasticsearch تبدیل نمود.

Kibana: یک ابزار تجسم و مدیریت برای Elasticsearch است که نمودار هیستوگرام، نمودار خط، نمودار دایره‌ای، و نقشه‌ها را فراهم می‌کند. Kibana همچنین شامل برنامه‌های پیشرفته‌ای می‌باشد که به کاربران اجازه می‌دهد تا به‌منظور تجسم بهتر داده‌های مکانی، اینفوگرافیک‌های پویا را به‌صورت سفارشی و براساس داده‌ها ایجاد کنند.

# Install Elastic Search

1- Install Java JDK : https://soft98.ir/software/692-sun-java-se-runtime-environment.html

2- Go to Advanced system settings -> Environment Variables -> system variable -> Path : add to Variable value  \;C:\Program Files\Java\jdk1.8.0_351\bin

3- Go To Elastic Site And Download & install  : https://artifacts.elastic.co/downloads/elasticsearch/elasticsearch-8.8.1-windows-x86_64.zip

4- unzip & run elasticsearch.bat  or install as service : a : run powershell as admin  b: goto path elasticsearch & run \bin\elasticsearch-service.bat install c: in services start or stop

4- localhost:9200 


# More 
تنظیمات امنیتی:

برای تعریف یوزر وپسورد برای Elasticsearch و Kibana، باید در انتهای فایل elasticsearch.yml در مسیر c:\elasticsearch-7.10.2\config، کد زیر را وارد کرد و سرویس Elasticsearch را ریستارت کرد :


xpack.security.enabled: true

سپس Powershell را اجرا کرده و مجدد به مسیر Elasticseach رفته و با استفاده از کد زیر برای یوزرهای پیش فرض Elasticsearch، پسورد تعیین کنید :


.\bin\elasticsearch-setup-passwords.bat interactive

می توان با استفاده از یوزر elastic وارد Kibana شده و یوزرها و Roleهای دلخواه خود را بر اساس نیاز، تعریف کرد.

تنظیمات سرور:

برای تنظیم Elasticsearch بر روی سرور، باید در فایل elasticsearch.yml خطوط زیر را اضافه کرد و سرویس Elasticsearch را ریستارت کرد
:

http.port: 9200

http.host: <serve-ip>
  
همینطور برای Kibana هم نیاز هست تا خط زیر در فایل Kibana.yml اضافه کرد :
  
server.host: <serve-ip>
  
  
در صورتی که برای Elasticsearch یوزر و پسورد تعریف کرده باشید، خطوط زیر نیز باید به فایل Kibana.yml اضافه گردد
  
  :
elasticsearch.username: "elastic"
  
elasticsearch.password: "Password"

