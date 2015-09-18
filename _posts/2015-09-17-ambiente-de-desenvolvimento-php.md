---
layout: post
title: "Ambiente de desenvolvimento PHP"
excerpt: "Antes de colocar a mão da massa, vou apresentar a lista do ingredientes necessários. Em outras palavras, vou apresentar quais ferramentas necessárias para montar um ambiente de desenvolvimento PHP."
modified: 2015-09-17
tags: [ambiente]
comments: true
---

Antes de colocar a mão da massa, vou apresentar a lista do ingredientes necessários. Em outras palavras, vou apresentar quais ferramentas necessárias para montar um ambiente de desenvolvimento PHP.

## Ferramentas

- Linux
- PHP
- Sublime Text 3
- Git


### Instalação do PHP

Nessa publicação irei ensinar a instalação do PHP no sistema operacional Linux. Como utilizo Ubuntu Desktop 14.04, pode haver pequenas diferenças em outras distruibuições.

Primeiramente vamos atualizar a lista de respositórios:

```
sudo apt-get update
```

Instalação do PHP-FPM (FastCGI Process Manager, ou em pt-BR Gerenciador de Processos FastCGI):

```
sudo sudo apt-get install php5-fpm
```

Instalação de algumas bibliotecas PHP:

```
sudo apt-get install php5-cli php5-curl php5-gd php5-imagick php-apc
```

### Instalação do Sublime Text 3

Acesse o site oficial do [Sublime Text](http://www.sublimetext.com/3), baixe o arquivo `.deb` de acordo com seu processador.

### Instalação do Git

```
sudo apt-get install git
```

## Hello, World

Se não existir, crie o diretório `/var/www/`. Crie o arquivo `index.php` e nele coloque:

``` php
<?php 
echo "Hello, world!";
```

Para visualizar o resultado, basta acessar seu diretório `/var/www` e executar o comando:

```
php -S localhost:8000
```

Agora acesse pelo navegador o endereço e porta informados `http://localhost:8000`.