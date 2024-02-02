# Debian Linux Command Utility
آموزش نصب و دستورات کاربردی بر روی سرور دبیان لینوکس


1. **ایجاد پوشه:**
   ```bash
   mkdir نام_پوشه
   ```

2. **ایجاد فایل:**
   ```bash
   nano نام_فایل
   ```

3. **لیست فایل‌ها:**
   ```bash
   ls
   ```

4. **لیست فایل‌های مخفی:**
   ```bash
   ls -a
   ```

5. **اعطای دسترسی به پوشه یا فایل:**
   ```bash
   chmod permissions نام_پوشه_یا_فایل
   ```

6. **حذف فایل:**
   ```bash
   rm نام_فایل
   ```

7. **حذف پوشه با تمامی اطلاعات داخل:**
   ```bash
   rm -r نام_پوشه
   ```

8. **مشاهده لیست ایمیج‌های داکر:**
   ```bash
   docker images
   docker ps -a
   ```

9. **حذف یک داکر براساس نام:**
   ```bash
   docker rmi نام_ایمیج
   ```

10. **حذف یک داکر براساس آی‌دی:**
    ```bash
    docker rmi آی‌دی_ایمیج
    ```

11. **نصب Docker:**
    برای نصب Docker در Debian، می‌توانید از دستورات زیر استفاده کنید:
    ```bash
    sudo apt update
    sudo apt install docker.io
    ```

12. **نصب Docker Compose:**
    برای نصب Docker Compose:
    ```bash
    sudo apt install docker-compose
    ```

