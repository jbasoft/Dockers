To install Sql Server in Debian Server in port 1443

برای نصب SQL Server در یک محیط Docker روی سرور Debian، می‌توانید از دستورات زیر استفاده کنید. ابتدا اطمینان حاصل کنید که Docker روی سیستم شما نصب شده باشد.

**1. دانلود تصویر Docker از Microsoft:**
```
   sudo docker pull mcr.microsoft.com/mssql/server
```

**2. اجرای یک محیط Docker با تنظیمات مربوط به SQL Server:**
```
   sudo docker run -e 'ACCEPT_EULA=Y' -e 'SA_PASSWORD=YourPassword' -p 1433:1433 --name sql_server_container -d mcr.microsoft.com/mssql/server
```

   در اینجا `YourPassword` را با گذرواژه مورد نظر خود جایگزین کنید.

**3. بررسی وضعیت اجرای کانتینر:**
```
   sudo docker ps -a
```

   اگر کانتینر با وضعیت "Up" نشان داده شود، به این معناست که SQL Server با موفقیت اجرا شده است.

حالا می‌توانید از ابزارهای مدیریت دیتابیس SQL Server به کانتینر متصل شوید و مدیریت دیتابیس خود را انجام دهید.
