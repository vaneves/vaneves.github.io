---
layout: post
title: "Guia de Estilo de Código"
excerpt: "Como falei na primeira publicação do blog, o PHP não é bagunçado, os programadores que são bagunçados com seus códigos. Mas cada programador, ou grupo de programadores, tem sua forma de organização."
modified: 2015-09-18
tags: [psr, formatação, estilo]
comments: true
---

Como falei na [primeira publicação do blog](/bem-vindo-ao-blog), o PHP não é bagunçado, os programadores que são bagunçados com seus códigos. Mas cada programador, ou grupo de programadores, tem sua forma de organização, afinal você pode criar a classe `User` de diversas maneiras:

``` php
<?php 
class User 
{
	public function getName() { //comments
	}
}

# comments
class User {
	public function get_name() {
	}
}

/* comments */
class Vendor_User 
{
	public function getName() 
	{
	}
}
```

Comumente os programadores PHP utilizam diversas bibliotecas e componentes em um mesmo projeto, na qual, se cada grupo/pessoa utilizar seu próprio estilo, o desenvolvido fica estranho e dificultoso. Então em 2009 uma galera se juntou e criou o [PHP-FIG](http://www.php-fig.org/) (PHP Framework Interop Group). O grupo criou (e continua aprimorando) um conjunto de guias de estilo de código, conhecidos como [PSR](http://www.php-fig.org/psr/) (PHP Standard Recommendation).

As PSRs são ~~obrigações~~ recomendações, mas todos os desenvolvedores PHP devem seguir, pois por meio delas a facilidade de entendimento e integração entre framework, bibliotecas e componentes são incríveis.

- **PSR-0:** Define como os arquivos serão "carregados" na aplicação, a técnica usada é chamada de autoloader;
- **PSR-1:** Define o padrão básico de codificação, como a tag PHP, codifiação do arquivo, nome dos métodos, etc.;
- **PSR-2:** Define o guia de estilo de codificação, como identação, declaração de namespace, classes, propriedades, métodos, etc.;
- **PSR-3:** Define uma interface para Loggers;
- **PSR-4:** Define como os arquivos serão "carregados" na aplicação. É recomendada para novos projetos. Projetos que usam a PSR-0 se possível, devem ser migrados para a PSR-4;
- **PSR-7:** Define um conjunto de interfaces comuns de mensagens HTTP.

E as PSRs 5 e 6? Na verdade já são 11 (de 0 à 10) até agora, porém algumas ainda estão em processo de criação.

## Conclusão

Um dos maiores ~~polêmicas~~ dilemas no mundo da programação é se quebra ou não a linha depois do `if`. Nós, desenvolvedores PHP, sabemos que não.