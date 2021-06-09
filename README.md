### &emsp; &emsp; به نام خدا ###
### &emsp; یدالله حبیب کاظمی ###
### تمرین 9 آزمایشگاه سیستم های عامل ###
<br>

__سوال 1 : بررسی کنید دستورات زیر چه می کنند و سه مورد از گزینه هایشان را توضیح دهید__

`chown`:

با این دستور قادر خواهید بود مالک و گروه ، فایل ها و دایرکتوری ها را تغییر دهید

`chown -R`:

تغییر اعمالی را بصورت بازگشتی بر روی تمامی فایل ها و دایرکتوری های داخل فایل

یا دایرکتوری موردنظرمان اعمال می کند

`chown -v`:

تغییرات اعمال شده را نمایش می دهد

`chown -c`:

مانند دستور قبلی عمل می کند با این تفاوت که 

فقط در صورتی که تغییری ایجاد شود گزارش می دهد

`gpasswd`:

با این دستور میتوان گروه ها را مدیریت کرد ، برای تغییر در خود یا کاربران گروه 

و مشخص کردن رمز از این دستور استفاده خواهد شد

`gpasswd -a`:

اضافه کردن کاربر به گروه

`gpasswd -r`:

حذف رمز گروه 

`gpasswd -d`:

حذف کاربر از گروه
<br><br>

__سوال 2 : نام و شماره کاربری و شماره گروه خود را بدست اورید__

با دستور زیر نام کاربر فعلی یا خودمان را مشاهده می کنیم

`whoami`

سپس خروجی را در دستور زیر گذاشته و اطلاعات کامل را مشاهده می کنیم 

`id yadollah`
<br><br>

__سوال 3 : یک حساب کاربری ایجاد و با رمز 25 ایجاد کنید__

ابتدا با دستور زیر کاربر مورد نظر را ایجاد میکنیم

`sudo useradd oslab`

سپس با دستور زیر برای آن رمز میگذاریم

`sudo passwd oslab`
<br><br>

__سوال 4 : دو گروه ایجاد کرده و حساب کاربری سوال قبل را به هر دو اضافه کنید و ادمین گروه سجاد قراردهید__

ابتدا با دو سدتور زیر دو گروه مورد نظر را ایجاد می کنیم

`sudo groupadd sadjad`

`sudo groupadd Uni`

سپس با دستور زیر کاربر مورد نظر را به این 2 گروه اضافه میکنیم

`sudo usermod -G sadjad,Uni oslab`

و در نهایت با دستور زیر کاربر را ادمین گروه سجاد میکنیم

`sudo gpasswd -A oslab sadjad`
<br><br>

__سوال 5 :کاربر دیگری ساخته آن را به گروه سجاد اضافه کنید و سپس این حساب را حذف کنید__

ابتدا با دستور زیر حساب کاربری مورد نظر را میسازیم

`sudo useradd os2`

سپس با دستور زیر کاربر ره به گروه سجاد اضافه میکنیم

`sudo usermod -G sadjad os2`

و در نهایت با دستور زیر کاربر را حذف میکنیم

`sudo userdel os2`
