---
layout: post
title: "Interface de Linha de Comando"
excerpt: "Antes de colocar a mão da massa, vamos juntar os ingredientes."
modified: 2015-09-17
tags: [ambiente]
comments: true
---

O PHP foi escrito para trabalhar no ambiente web (por meio de um navegador), porém pode ser utilizado pela interface de linha de comando (terminal), auxiliando na automatização de tarefas. 

Vejamos um exemplo de PHP via linha de comando utilizando argumentos. Crie o arquivo `hello.php`:

{% highlight php %}
<?php
if ($argc != 2) {
    echo "Usage: php hello.php [name].\n";
    exit(1);
}
$name = $argv[1];
echo "Hello, $name\n";
{% endhighlight %}

As variáveis `$argc` e `$argv` são criadas automaticamente pelo PHP, na qual guardam informações referentes aos argumentos. A variável `$argc` contém a quantidade de argumentos informados. Já a `$argv` é um *array* que contém os valores dos argumentos. O primeiro argumento sempre é o nome do arquivo, no caso `hello.php`.

A função `exit();` encerra a execução do script. O parâmetro zero indica ao shell se a execução falhou.

Para executar nosso script acima, a partir da linha de comando:

{% highlight text %}
php hello.php
Usage: php hello.php [name]
{% endhighlight %}

{% highlight text %}
php hello.php world
Hello, world
{% endhighlight %}