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

```
