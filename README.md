# CakePHP Application Skeleton

![Build Status](https://github.com/cakephp/app/actions/workflows/ci.yml/badge.svg?branch=5.x)
[![Total Downloads](https://img.shields.io/packagist/dt/cakephp/app.svg?style=flat-square)](https://packagist.org/packages/cakephp/app)
[![PHPStan](https://img.shields.io/badge/PHPStan-level%208-brightgreen.svg?style=flat-square)](https://github.com/phpstan/phpstan)

A skeleton for creating applications with [CakePHP](https://cakephp.org) 5.x.

The framework source code can be found here: [cakephp/cakephp](https://github.com/cakephp/cakephp).

## Installation

1. Download [Composer](https://getcomposer.org/doc/00-intro.md) or update `composer self-update`.
2. Run `php composer.phar create-project --prefer-dist cakephp/app [app_name]`.

If Composer is installed globally, run

```bash
composer create-project --prefer-dist cakephp/app
```

In case you want to use a custom app dir name (e.g. `/myapp/`):

```bash
composer create-project --prefer-dist cakephp/app myapp
```

You can now either use your machine's webserver to view the default home page, or start
up the built-in webserver with:

```bash
bin/cake server -p 8765
```

Then visit `http://localhost:8765` to see the welcome page.

Usage
After installation, you can access the application at:
Product listing: http://localhost:8765/products
Add new product: http://localhost:8765/products/add

## Update

CakePHP 5 Inventory Tracker
This application is an inventory management system built with CakePHP 5. It allows users to manage product inventory with specific constraints and features.
Installation
Clone the repository:

## Configuration

text
git: [[repository-url](https://github.com/lucasvalenca1/Cake.php-Inventory-tracker_002)] cakephp-app inventory-tracker
cd inventory-tracker
Install dependencies:

## Composer

php composer.phar install
Set up the database: Configure your database in config/app_local.php. Run the migrations:

## CakePHP Migrations

bin/cake migrations migrate
Start the server:

## CakePHP Server

Seed the database:
text
bin/cake migrations seed

Read and edit the environment specific `config/app_local.php` and set up the
`'Datasources'` and any other configuration relevant for your application.
Other environment agnostic settings can be changed in `config/app.php`.

Features
Product management (add, edit, list, delete)
Custom validation rules
Dynamic status calculation
Search and filter functionality
Soft delete implementation

Model: Product
Fields:
id
name
quantity
price
status (in stock, low stock, out of stock)
Validation Rules:
name: Required, unique, 3-50 characters
quantity: Integer, 0-1000
price: Decimal, > 0, <= 10,000
Custom rules:
Products with price > 100 must have quantity >= 10
Products with "promo" in name must have price < 50

Database Seeding
The application comes with a seeder that populates the database with 10 sample products. To run the seeder:
text
bin/cake migrations seed
Unit Tests
To run the unit tests:
text
vendor/bin/phpunit

Requirements Review
Product Model with specified fields
Validation rules implemented
Custom validation rules added
ProductsController with required actions
Views for listing, adding, and editing products
Dynamic status calculation
Search and filter functionality
Pagination implemented
Soft delete functionality
Automatic last_updated field update
Unit test suite
Database seeding with sample products
All requirements have been met and implemented in this CakePHP 5 application.

## Layout

The app skeleton uses [Milligram](https://milligram.io/) (v1.3) minimalist CSS
framework by default. You can, however, replace it with any other library or
custom styles.
