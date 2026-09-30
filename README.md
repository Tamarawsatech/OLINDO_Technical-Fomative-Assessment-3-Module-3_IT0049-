# CodeIgniter POS TFA3

## Description

This CodeIgniter 4 POS application provides validated customer and user forms,
edit/update functionality, and prepared user avatar uploads.

## Features

- Customer listing, creation, editing, and validation
- User listing, creation, editing, and unique username validation
- JPG/PNG avatar uploads up to 2 MB
- 300 by 300 prepared avatars and a default placeholder
- Database export in `database/pos_tfa2.sql`

## Requirements

- PHP 8.1 or later with the GD extension
- MySQL or MariaDB
- Composer
- Apache with mod_rewrite enabled

## Local Installation

1. Start Apache and MySQL in XAMPP.
2. Import `database/pos_tfa2.sql` in phpMyAdmin.
3. Confirm `.env` uses database `pos_tfa2`, username `root`, and a blank local password.
4. Run `composer install` if `vendor/` is not present.
5. Ensure `public/uploads/avatars` is writable.
6. Open `http://localhost/OLINDO/codeigniter-project/public/`.

The local `.env` must contain:

```ini
CI_ENVIRONMENT = development
app.baseURL = 'http://localhost/OLINDO/codeigniter-project/public/'
database.default.hostname = localhost
database.default.database = pos_tfa2
database.default.username = root
database.default.password =
database.default.DBDriver = MySQLi
database.default.DBPrefix =
database.default.port = 3306
```

Do not commit `.env`; it is ignored because it may contain hosting credentials.

## Routes

- `/customers`, `/customers/new`, `/customers/edit/{id}`
- `/users`, `/users/new`, `/users/edit/{id}`

Run `php spark routes` to verify the route table.
