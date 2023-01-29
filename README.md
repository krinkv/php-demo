# Prerequisities

1. install composer - 'sudo apt install composer'

2. run - 'composer require firebase/php-jwt' to install jwt library

# DB setup
Create new php_auth database from phpmyadmin.

Run the following script to create the user table

CREATE TABLE `users` (
 `id` int(11) NOT NULL AUTO_INCREMENT,
 `name` varchar(50) COLLATE utf8mb4_unicode_ci NOT NULL,
 `email` varchar(50) COLLATE utf8mb4_unicode_ci NOT NULL,
 `password` varchar(150) COLLATE utf8mb4_unicode_ci NOT NULL,
 PRIMARY KEY (`id`),
 UNIQUE KEY `email` (`email`)
) ENGINE=InnoDB AUTO_INCREMENT=6 DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_unicode_ci;

Copy new php-auth-api directory in htdocs in xampp

# Testing
Via postman hit 
http://localhost/php-auth-api/register.php
with request body
{
	"name":"username",
    "email":"useremail@mail.com",
    "password":"user password"
}


http://localhost/php-auth-api/login.php
with request body
{
    "email":"useremail@mail.com",
    "password":"user password"
}