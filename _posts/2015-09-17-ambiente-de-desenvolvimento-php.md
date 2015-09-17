---
layout: post
title: "Ambiente de desenvolvimento PHP"
excerpt: "Antes de colocar a mão da massa, vamos juntar os ingredientes."
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

{% highlight text %}
sudo apt-get update
{% endhighlight %}

Instalação do PHP-FPM (FastCGI Process Manager, ou em pt-BR Gerenciador de Processos FastCGI):

{% highlight text %}
sudo sudo apt-get install php5-fpm
{% endhighlight %}

Instalação de algumas bibliotecas PHP:

{% highlight text %}
sudo apt-get install php5-cli php5-curl php5-gd php5-imagick php-apc
{% endhighlight %}

### Instalação do Sublime Text 3

Acesse o site oficial do [Sublime Text](http://www.sublimetext.com/3), baixe o arquivo `.deb` de acordo com seu processador.

### Instalação do Git

{% highlight text %}
sudo apt-get install git
{% endhighlight %}

## Hello, World

Se não existir, crie o diretório `/var/www/`. Crie o arquivo `index.php` e nele coloque:

{% highlight php %}
<?php 
echo "Hello, world!";
{% endhighlight %}

Para visualizar o resultado, basta acessar seu diretório `/var/www` e executar o comando:

{% highlight text %}
php -S localhost:8000
{% endhighlight %}

Agora acesse pelo navegador o endereço e porta informados `http://localhost:8000`.