---
layout: post
title: "Variáveis, Contantes e Operadores"
excerpt: "Finalmente vamos por a mão na massa e entrar nos conceitos básicos da linguagem. O PHP muda das demais linguagens não somente a sintaxe, aqui verá algo um pouco diferente, que no começo pode até assustar, mas depois que pegar o jeito, vai gostar."
modified: 2015-09-18
tags: [php, constante, variáveis, lógica de programação]
comments: true
---

Finalmente vamos por a mão na massa e entrar nos conceitos básicos da linguagem. O PHP muda das demais linguagens não somente a sintaxe, aqui verá algo um pouco diferente, que no começo pode até assustar, mas depois que pegar o jeito, vai gostar.

## Variáveis e Constantes

Primeiramente, o PHP é uma linguagem fracamente tipada. Em outras palavras, você não define o tipo da variável, o PHP automaticamente detecta e define o tipo dela.

``` php
<?php 
$course 	= 'Desenvolvimento Web com PHP e AngularJS';
$vacancies	= 15;
$its_full	= false;
$price		= 50.0;
$trainers	= ['Van Neves', "Diego Oliveira"];
$start_date	= new DateTime('2015-10-26');
$end_date	= null;
```

No exemplo acima utilizei quase todos os tipos de variáveis disponíveis no PHP, ainda faltaram o `resource` e o `callback`. Não, o PHP não tem `char` e você pode utilizar aspas duplas ou simples (apóstrofe) para `string`.

Uma variável pode mudar o tipo quando assume outro valor. Por exemplo:

``` php
<?php 
$a = 'Texto'; //$a é string
$a = 1; //$a agora é integer
```

As variáveis PHP são case-sensitive, ou seja, diferencia maiúsculas dé minúsculas. Por exemplo `$name` é diferente de `$Name` e de `$NAME`.

### Constantes

Diferentemente de uma variável, a constante não pode ter seu valor alterado. Para criar uma constante você deve utilizar a função `define()`, que recebe dois parâmetros: nome da contante; valor da constante. Veja:

``` php
<?php 
define('CODE_SUCCESS', 1);
define('CODE_ERROR', 0);
```

Utilizando uma constante:

``` php
<?php 
echo CODE_SUCCESS;
```

Assim como as variáveis, as contantes são case-sensitives, mas por boas práticas (como vimos na publicação anteior), sempre deve-se usar MAIÚSCULA. Há também outra maneira de definirmos constante, dentro de uma classe, porém veremos apenas em publicações futuras.

Se você tentar declarar duas contantes com o mesmo nome, o PHP irá desparar um erro. Portanto, a função `defined()` verifica se uma constante já foi definida anteriormente.

``` php
<?php 
if(defined('CODE_SUCCESS') == false) {
	define('CODE_SUCCESS', 1);
}
```

## Operadores

Precisa mesmo desse tópico? Sim, mas simplemente por causa da concatenação, pois isso pode ficar meio confuso no começo.

Diferentemente de outras linguagens, para concatenar duas strings no PHP você utiliza o `.` e não o sinal de `+`. Por quê? PHP, lá na sua criação, nasceu de outra linguagem, o Perl, que já usava o `.` para concatenar, então ficou. Veja um exemplo:

``` php
<?php
$first_name = 'Van';
$last_name = 'Neves';

echo 'Meu nome é ' . $first_name . $last_name;
```

Saída:

``` php
Meu nome é VanNeves
``` 

Como falei no tópico anteior, o PHP é uma linguagem fracamente tipada, então se você tentar utilizar o `+` para concatenar (se não tiver constume vai fazer isso muito) ele irá na verdade converter a string em número e tentar somar. Por exemplo:

``` php
<?php
$first_name = 'Van';
$last_name = 'Neves';

echo 'Meu nome é ' + $first_name + $last_name;
```

Saída:

``` php
0
``` 

Isso porque o PHP pega a string, se ela começar com números, ele converte os números, se não começar com números, ele converte em `0`. Isso leva até há uma brincadeira comum entre os instrutores de PHP:


``` php
<?php
$animal1 = '1 gato';
$animal2 = '3 gatos';

echo $animal1 + $animal2;
```

Saída:

``` php
4
``` 

Comos ambas strings começam com números, eles são convertidos e somados.

## Conclusão

O PHP é estranho, não é? Não! É questão de costume e você provavelmente está familiarizado com outra linguagem. O PHP tem uma sintaxe diferente do Ruby, que por sua vez é diferente do Objective-C, que se difere do Java, etc.