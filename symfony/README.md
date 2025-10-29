# Symfony

## First Steps

https://symfonycasts.com/screencast/symfony/setup

```bash
# install on mac
# https://symfony.com/download
brew install symfony-cli/tap/symfony-cli

# help, available symfony commands list
symfony --help

# check availoable system requirements
symfony check:req

# set up new symfony app 'starshop'
symfony new starshop

# start local server
cd starshop
symfony serve

# install SSL support (TLS support)
symfony server:ca:install

# https://127.0.0.1:8000/

```

**Github notes**

Shop set up as submodule to existing repositoty:

```bash
git submodule add https://github.com/schafeld/PHP-Experiments symfony/starshop
```

**Funny stuff with Symfony and PHP**
```bash
# delete /vendor directory
# app broken
cd /starshop
composer install
# all works again

# install code style fixer
composer require cs-fixer-shim

# Symfony auto-linting
# show cs fixer commands
./vendor/bin/php-cs-fixer
# fix styles
./vendor/bin/php-cs-fixer fix

```


## Additions

```bash
# add Twig templating
composer require twig

# Add debugger
composer require debug

# Debug via console
./bin/console
# or
php bin/console

# debug routes
./bin/console debug:router
# or
php bin/console debug:router
# or
symfony console debug:router

# Show available Twig functions, filters ...
# or
php bin/console debug:twig

# Find available services in container
./bin/console debug:container

# display service shortcuts
./bin/console debug:autowiring
# search for a specific service about logging
./bin/console debug:autowiring log

# Asset Mapper
composer require symfony/asset-mapper
# debug assets, show available asset file paths
# in locations declared in asset_mapper.yaml
./bin/console debug:asset

# Add Tailwind
composer require symfonycasts/tailwind-bundle
# configure tailwind
./bin/console tailwind:init
# build Tailwind (watch mode)
./bin/console tailwind:build -w
# configured in .symfony.local.yaml to auto-start with server
symfony serve

# Clear Cache – e.g. when template changes are not being rendered:
php bin/console cache:clear

```
