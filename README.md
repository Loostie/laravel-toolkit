# laravel-toolkit

![laraveltk](https://images2.imgbox.com/a3/8b/CmtS67rN_o.png)

A set of tools for managing laravel on your server

What Laravel Toolkit will do:

- Check for PHP and install if not present
- Check for [Composer](https://github.com/composer/composer) and install if not present

What Laravel Toolkit can do:

- Install [NGINX](https://www.nginx.com)
- Install and automatically configure [MySQL](https://www.mysql.com)
- Create a new Laravel Application
  - With database (also changes .env) - optional
  - With NGINX config (http/https) - optional

## Installation

1. `git clone https://github.com/Loostie/laravel-toolkit.git`
2. `cd laravel-toolkit`
3. `sudo chmod +x laraveltk`
4. `sudo ./laraveltk`

## Configuration

If you open `laraveltk` you'll see this at the top:

```bash
#Change this to your desired version
install_php="8.2"
# Change this your desired projects path
project_path="/home/projects/"
```

Here you can change what PHP version laraveltk will install on first launch (if you do not have PHP already installed) and where laraveltk will place your application folders when creating a new laravel app

If you open `db.config` you'll see this:

```bash
#If you already have MySQL installed, enter credentials here
#If NOT, you can install it with the toolkit first, then come back

DBHOST=127.0.0.1
DBPORT=3306
DBUSER=root
DBPASS=
```

Here you'll need to change the database connection info, if you already have MySQL installed you can change this immediately, if not, change this after you've installed it using laraveltk

## Important

- This tool is created and tested for Ubuntu 22.04 (Jammy Jellyfish)
(It will most likely work on older versions of Ubuntu)
- laraveltk needs to be ran in the same folder with `db.config` and the `templates` folder
