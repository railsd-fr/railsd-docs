---
title: Installation de Ruby on Rails
description: Installation de Ruby on Rails sur Ubuntu 22.04 LTS et macOS.
---

Installation de Ruby, Ruby on Rails et PostgreSQL sur Ubuntu 22.04 LTS et macOS.

---

## Installation sur Ubuntu 22.04 LTS

### Installation de Ruby

Installer les pré-requis :

```shell
sudo apt install autoconf bison build-essential libssl-dev libyaml-dev libreadline6-dev zlib1g-dev libgmp-dev libncurses5-dev libffi-dev libgdbm6 libgdbm-dev libdb-dev uuid-dev
```

Installer rbenv :

```shell
git clone https://github.com/rbenv/rbenv.git ~/.rbenv
echo 'eval "$(~/.rbenv/bin/rbenv init - bash)"' >> ~/.bashrc
exec $SHELL
```

Installer ruby-build :

```shell
git clone https://github.com/rbenv/ruby-build.git "$(rbenv root)"/plugins/ruby-build
echo 'export PATH="$HOME/.rbenv/plugins/ruby-build/bin:$PATH"' >> ~/.bashrc
exec $SHELL
```

Installer Ruby 3.1.2 :

```shell
rbenv global 3.1.2
```

Vérifier la bonne installation de Ruby :

```shell
ruby -v
```

Installer Bundler :

```shell
gem install bundler
```

### Installation de Ruby on Rails

Installer la dernière version de Ruby on Rails :

```shell
gem install rails
```

Rendre l'exécutable de Rails disponible :

```shell
rbenv rehash
```

### Installation de PostgreSQL

Installer PostgreSQL :

```shell
sudo apt install postgresql-14 libpq-dev
```

Créer un super-utilisateur PostgreSQL :

```shell
sudo -u postgres createuser developer -s
```

Sécuriser le super-utilisateur PostgreSQL :

```shell
sudo -u postgres psql
\password developer
```

---

## Installation sur macOS

### Installation de Ruby

Installer Homebrew :

```shell
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

Installer rbenv et ruby-build :

```shell
brew install rbenv ruby-build
```

Installer Ruby 3.1.2 :

```shell
rbenv global 3.1.2
```

Vérifier la bonne installation de Ruby :

```shell
ruby -v
```

Installer Bundler :

```shell
gem install bundler
```

### Installation de Ruby on Rails

Installer la dernière version de Ruby on Rails :

```shell
gem install rails
```

Rendre l'exécutable de Rails disponible :

```shell
rbenv rehash
```

### Installation de PostgreSQL

Installer PostgreSQL :

```shell
brew install postgresql
```

