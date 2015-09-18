---
layout: post
title: "Bem-vindo ao Blog"
excerpt: "Seja bem-vindo ao meu blog. Vou começar essa publicação contando uma história que aconteceu em 2008, na época em que eu ainda fazia faculdade de Sistemas de Informação."
modified: 2015-09-16
tags: [foo bar, hello world, php]
comments: true
---

Seja bem-vindo ao meu blog. Vou começar essa publicação contando uma história que aconteceu em 2008, na época em que eu ainda fazia faculdade de Sistemas de Informação. Eu estava desenvolvendo uma aplicação em PHP e um outro estudante, ao ver, fez o seguinte comentário:

> Cara, o PHP não presta, é muito bagunçado, é código estranho, uma página inclui outra, que inclui outra e por ai vai.

Eu não tive outra reação a não ser dizer a verdade na cara dele:

> Me desculpe, mas o PHP não é bagunçado, você é bagunçado, seu código que é mal feito.

Tudo bem que meu código não era o melhor do mundo, mas já tentava ao máximo, de acordo com meu nível de conhecimento, deixar tudo nos trinques, então mostrei à ele. Eu utilizava uma [classe de template](http://raelcunha.com/template.php), criada por Rael Cunha, para separação do código PHP da interface HTML. Também utilizava classes DAO (Data Access Object) para manipular o banco de dados. Minha estrutura era algo do tipo:

```
index.php
cliente.php
config.php
inc/
	Conexao.class.php
	Template.class.php
	Filtro.functions.php
DAO/
	Cliente.class.php
	ClienteDAO.class.php
tpl/
	template.html
	cliente-lista.html
	cliente-cadastro.html
```

Como falei, não era nem de longe a coisa mais organizada do mundo, mas também não era bagunçado, qualquer que pegasse o código conseguia dar continuidade.

Sete anos se passaram desde o acontecido, mas ainda hoje vejo muitas pessoas praticando e ensinando o PHP com códigos bagunçados e principalmente com falhas de segurança. Isso me motivou a criação deste blog, para levar às pessoas como desenvolver aplicações em PHP utilizando boas práticas.