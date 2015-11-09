---
layout: post
title: "Condicionais"
excerpt: "Hoje vamos falar sobre condicionais em PHP. Para quem já está acostumado com outras linguagens pode estranhar um pouco no começo."
modified: 2015-11-08
tags: [php, condicionais]
comments: true
---

Hoje vamos falar sobre condicionais em PHP. Para quem já está acostumado com outras linguagens pode estranhar um pouco no começo, pois no PHP vamos além do *booleano* (`true` e `false`).

## Condicionais

Como falei na publicação anterior, o PHP é uma linguagem fracatamente tipada, sendo assim os condicionais (`if`, `while`, ...) vão além dos booleanos. Em linguagens fortemente tipadas, como Java e C#, um `if` pode conter apenas booleanos, mesmo que seja comparando dois inteiros, como `1 == 1` o resultado é um *boleano*, no caso `true`.

Muita calma nessa hora. No PHP é possível dar como verdadeiro uma variável que tenha tenha mesmo que seja diferente de `true`, por exemplo:

```php
<?php
$course 	= 'Desenvolvimento Web com PHP e AngularJS';
$start_date	= new DateTime('2015-10-26');
$end_date	= null;
$its_full	= false;
$price		= 0;

// exemplo 1
if($course == true) {
	echo "Variável \$course possui valor\n";
} else {
	echo "Variável \$course NÃO possui valor\n";
}

// exemplo 2
if($start_date == true) {
	echo "Variável \$start_date possui valor\n";
} else {
	echo "Variável \$start_date NÃO possui valor\n";
}

// exemplo 3
if($end_date == true) {
	echo "Variável \$end_date possui valor\n";
} else {
	echo "Variável \$end_date NÃO possui valor\n";
}

// exemplo 4
if($its_full == true) {
	echo "Variável \$its_full possui valor\n";
} else {
	echo "Variável \$its_full NÃO possui valor\n";
}

// exemplo 5
if($price == true) {
	echo "Variável \$price possui valor\n";
} else {
	echo "Variável \$price NÃO possui valor\n";
}
```

Nos exemplos acima, as variáveis são testadas nos condicionais `if`. No **exemplo 1** é verificado se a variável `$course` possui valor. Em outras linguagens, fortemente tipadas, ocorreria um erro, pois a variável `$course` é uma *string* não é *booleana*. No caso, a saída seria:

```
Variável $course possui valor
```

O **exemplo 2** é igual ao anterior, só que no caso é testada a variável `$start_date`, que possui como valor um objeto `DateTime`. A saída é:

```
Variável $start_date possui valor
```

Já no **exemplo 3** a variável `$end_date` tem um valor `null`, portando não passa no teste condicional. No caso a saída é:

```
Variável $end_date NÃO possui valor
```

Bom, agora vamos à uma pequena surpresa. No **exemplo 4** a variável `$its_full` **possui** um valor, que foi definido `false`, porém além de testar se a variável possui valor ou não, no PHP o condicional ainda testa e valor é verdadeiro. Veja a saída:

```
Variável $its_full NÃO possui valor
```

No **exemplo 5** também temos uma surpresa. A variável `$price` é um inteiro e possui valor, no caso `0`, porém o valor também não é verdadeiro. A saída:

```
Variável $price NÃO possui valor
```

E agora, José? No PHP além do `==` temos o `===` (ou `!==`), nele testamos não somente os valores, mas os tipos dos valores. Por exemplo:

```php
if($course === true) {
	echo "Variável \$course é booleana e possui o valor true\n";
} else {
	echo "Variável \$course não é booleana ou não possui valor true\n";
}
```

No exemplo acima estamos testando se a variável `$course` possui valor e ele é  `true`. No caso a saída será:

```
Variável $course não é booleana ou não possui valor true
```

## Conclusão

No começo é meio estranho a forma que o PHP trata as variáveis em condicionais, mas quando se acostuma isso fica comum. E por que ele não trata nos `if`s apenas *booleanos*? Acredito que pela tipagem fraca, então isso foi muito importante no começo da linguagem.