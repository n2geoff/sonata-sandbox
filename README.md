# Sonata Sandbox

## WARNING: This repository is abandoned

There is no active support on it.

Feel free to ask if you want to help to keep this project up to date.

## What's inside?

Sonata Sandbox comes pre-configured with the following bundles:

* Bundles from Symfony Standard distribution
* Sonata Admin Bundles: Admin and Doctrine ORM Admin
* Sonata Ecommerce Bundles: Payment, Customer, Invoice, Order and Product
* Sonata Foundation Bundles: Notification, Formatter, Intl, Cache, Seo and Easy Extends
* Sonata Feature Bundles: Page, Media, News, User, Block, Timeline
* Api Bundles: FOSRestBundle, BazingaHateoasBundle, NelmioApiDocBundle and JMSSerializerBundle

## Installation

### Download sandbox files by one of possible examples

Git:

    git clone https://github.com/sonata-project/sandbox.git
    cd sandbox
    git checkout master

### Prepare configuration

* Copy configuration file: ``cp .env .env.local``
* Edit ``.env.local`` to configure own environment

### Install Composer

REQUIRES: PHP 7.4 as of 05/21/2025

1. run `composer install -n --no-scripts`
2. it should fail, eventually, then run `composer update symfony/flex`
3. run #1 again

### Load fixtures data

    vendor/bin/phing

* You should be ready to go ...


## Run

you can use symfony cli tool to start the demo:

    symfony server:start --port=9090

> DOWNLOAD: https://symfony.com/download?v&&QEOH1hOQezWiRgk=8rKL2DPv

Now open your browser and go to http://localhost:9090/

## Tests

### Functional testing

To run the Behat tests, copy the default configuration file and adjust the base_url to your needs

* Copy configuration file: ``cp behat.yml.dist behat.yml``
* Edit it ``behat.yml``

You can now run the tests suite by using the following command:

    bin/qa_behat.sh

To get more informations about Behat, feel free to check [the official documentation][link_behat].


### Unit testing

To run the sandbox test suites, you can run the command:

    vendor/bin/simple-phpunit

You can also run the whole sonata-project bundles test suites by using the following command:

    bin/qa_client_ci.sh

Enjoy!

[link_behat]: http://docs.behat.org "the official Behat documentation"
[link_sonata]: http://sonata.local "Sonata"
