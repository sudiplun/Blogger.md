**Install the Apache package**

![lamp](https://res.cloudinary.com/daewefkrz/image/upload/c_scale,h_277/v1686503549/Blog-Images/Web_Development/jd8stxv3qwleikpl6qgr.webp)

installation all packages

```bash
sudo dnf install httpd mariadb-server php
```

**Install PHP modules command by using the below command**

```bash
dnf install -y php-cli php-fpm php-common php-mbstring php-curl php-gd php-mysqlnd php-json php-xml php-intl php-pecl-apcu php-opcache
```

**Start Apache service by using the below command**

```bash
sudo systemctl start httpd
```

**Start MariaDB service by using the below command**

```
sudo systemctl start mariadb
```

**Enable Apache service by using the below command**

_if you want your `httpd` autostart on boot run below command._

```bash
sudo systemctl enable httpd
```

**Check Apache status by using the below command**

```bash
sudo systemctl status httpd
```

**Enable MariaDB by using the below command**

_if you want your `mariadb` autostart on boot run below command._

```bash
sudo systemctl enable mariadb
```

**Check MariaDB status by using the below command**

```bash
sudo systemctl status mariadb
```

---

**Install MySQL secure installation by using the below command**

```bash
sudo mysql_secure_installation
```

**Open MariaDB configuration file by using the below command**

```bash
sudo mysql -u root -p
```

**Now open the Apache configuration file and update the php test file by using the below command**

```bash
vim /var/www/html/test.php
```

<u>Additional command </u>

To stop a service like `httpd` or `mariadb` using systemctl, you can use the following command:

```bash
sudo systemctl stop httpd
```

Replace `httpd` with `mariadb` to stop it.

If you want to prevent the service from starting automatically at boot time, you can disable it using the following command:

```bash
sudo systemctl disable httpd
```

Replace `httpd` with `mariadb` for it.
