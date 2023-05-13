Dependencies
------
  * php
  * mysql-server
  * php-pdo\_mysql
  * php-gd (recommended, used for image compression)

Installing
------
Make sure you have the dependencies installed.

Edit the php.ini file (the config file related to your php installation) and uncomment the following line:
```
extension=pdo_mysql
```
If you installed php-gd, uncomment the following line:
```
extension=gd
```
and increment the max upload file size to 8MB:
```
upload_max_file_size = 8M
```
This is fine because image compression reduces the uploads' size by about 4 times with the compression settings we chose.

Next, edit the [config.ini](./config.ini) file to change the database connection credentials.

Finally, execute the [database creation script](./scripts/create_database.sql)

License
-------
This project is released under the terms of the AGPLv3 license. See [COPYING](./COPYING) for more details.
