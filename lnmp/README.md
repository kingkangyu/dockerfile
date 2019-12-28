
### build images with php7.3.6

```
docker build -f Dockerfile_php7 -t 'lnmp:php7' .
```

### build images with php5.6.40

```
docker build -f Dockerfile_php5 -t 'lnmp:php5' .
```

### open php log_error

php.ini

```
vi /usr/local/php/etc/php.ini
```

set
```
log_errors = On
error_log = /home/wwwlogs/php_errors.log
error_reporting=E_ALL
```

### PS
```
RUN echo -e "0\n9\n1\n" |./install.sh lnmp
```
0 stands for the choice of DataBase

9 stands for the choice of PHP

1  Memory Allocator

```
You have 11 options for your DataBase install.
1: Install MySQL 5.1.73
2: Install MySQL 5.5.62 (Default)
3: Install MySQL 5.6.44
4: Install MySQL 5.7.26
5: Install MySQL 8.0.13
6: Install MariaDB 5.5.63
7: Install MariaDB 10.0.38
8: Install MariaDB 10.1.40
9: Install MariaDB 10.2.24
10: Install MariaDB 10.3.15
0: DO NOT Install MySQL/MariaDB
Do not install MySQL/MariaDB!
===========================
You have 9 options for your PHP install.
1: Install PHP 5.2.17
2: Install PHP 5.3.29
3: Install PHP 5.4.45
4: Install PHP 5.5.38
5: Install PHP 5.6.40 (Default)
6: Install PHP 7.0.33
7: Install PHP 7.1.30
8: Install PHP 7.2.19
9: Install PHP 7.3.6
You will install PHP 7.3.6
===========================
You have 3 options for your Memory Allocator install.
1: Don't install Memory Allocator. (Default)
2: Install Jemalloc
3: Install TCMalloc
You will install not install Memory Allocator.

```
