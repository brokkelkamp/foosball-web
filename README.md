# foosball-web

Web application that keeps track of foosball ratings.

## Installation

Requires any web server with php and SQL

To use nginx with sqlite3 on Arch linux:

- Install the required packages

    `pacman -S nginx php-fpm php-sqlite`

- Uncomment the `extension=pdo_sqlite` line in `/etc/php/php.ini`

- Follow the instructions at https://wiki.archlinux.org/index.php/nginx#FastCGI to enable PHP in nginx

- Set a password in `admin/phpliteadmin.config.php`

- Initialize the database

    `sqlite3 -init create_database.sql backend/foos.db`

- Make sure php can write to the database and the directory it is in

    `chown http backend`
    `chown http backend/foos.db`

