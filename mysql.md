# MySQL

## Install

> sudo apt-get install mysql-server -y

## Configure

> sudo mysql_secure_installation

## Check status:

> systemctl status mysql.service
or
> sudo mysqladmin -p -r root version

## Allowing root to connect via password

> sudo mysql
> SELECT user,authentication_string,plugin,host FROM mysql.user;
> ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'password';
> FLUSH PRIVILEGES;
> exit;

## Importing .sql file

> mysql -u <user> -p database_name < file.sql
>  
> Or, inside MySQL:
>  
> source file.sql
