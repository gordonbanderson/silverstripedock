# SilverStripe Dock
**** EXPERIMENTAL ****
## Introduction
Fork of Laradock to work with SilverStripe projects

## Install and Run Containers
```
composer create-project silverstripe/installer testsilverdock
cd testsilverdock
git init
git submodule add https://github.com/gordonbanderson/silverstripedock.git
cd silverstripedock
cp env-example .env
sudo docker-compose up -d nginx mariadb adminer workspace
```

## Install SilverStripe
After running composer install on a clean project, one can access the database with the
credentials in the .env file (default is root/root).  The server name is the docker-compose
container name, so in the above example it is mariadb.

Go to http://localhost:80/ to install your site.

Note that redirection to the CMS is currently broken (page not found).  Manually go to
http://localhost/admin/pages and login with the credentials used during install.
