---
layout: post
title: "Interface de Linha de Comando"
excerpt: "O PHP foi escrito para trabalhar no ambiente web (por meio de um navegador), mas também pode ser utilizado pela interface de linha de comando (Command Line Interface, ou CLI), auxiliando na automatização de tarefas."
modified: 2015-09-17
tags: [php, cli, shell]
comments: true
---

O PHP foi escrito para trabalhar no ambiente web (por meio de um navegador), mas também pode ser utilizado pela interface de linha de comando (Command Line Interface, ou CLI), auxiliando na automatização de tarefas. 

Vejamos um exemplo de script PHP via linha de comando utilizando argumentos. Basta criar o arquivo `hello.php` e inserir o seguinte código:

``` php
<?php
if ($argc != 2) {
    echo "Usage: php hello.php [name].\n";
    exit(1);
}
$name = $argv[1];
echo "Hello, $name\n";
```

As variáveis `$argc` e `$argv` são criadas automaticamente pelo PHP, na qual guardam informações referentes aos argumentos. A variável `$argc` contém a quantidade de argumentos informados. Já a `$argv` é um *array* que contém os valores dos argumentos. O primeiro argumento sempre é o nome do arquivo, no caso `hello.php`.

A função `exit();` encerra a execução do script. O parâmetro zero indica ao shell se a execução falhou.

Para executar nosso script acima, a partir da linha de comando:

```
php hello.php world
Hello, world
```

O `if` verifica se o argumento esperado foi realmente informado, caso contrário ele exibe uma mensagem.

```
php hello.php
Usage: php hello.php [name]
```

Vale lembrar que os argumentos são separados por espaços. Portanto, para enviar um único argumento que contenha espaço, como nome composto, deve-se usar aspas. Por exemplo `"Ana Julia"`. Outro fator importante é restringir o acesso aos arquivos CLI pelo navegador.

O PHP CLI suporta, também, interface interativa, como Python e Ruby, por meio do Shell Interativo, basta utilizar a opção `-a`. Clique [aqui](http://php.net/features.commandline.options) e veja mais opções.

## Conclusão

Conhecendo os recursos do PHP, é possível obter resultados incríveis. Por exemplo, você pode utilizar o PHP CLI para executar um script instalador de uma aplicação ou agendar tarefas no cron.