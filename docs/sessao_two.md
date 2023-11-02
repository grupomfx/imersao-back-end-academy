---
title: Retomando Conceitos do Linguagem JS (Part I)
authors:
    - Rodrigo Becker
date: 2023-11-01
some_url: https://example.com
---

# Retomando Conceitos do Linguagem JS (Part I) 📙


### Afinal o que é o Javascript?

Javascript é uma linguagem de programação, E como todas as demais linguagens de programação funciona traduzindo sintaxe 
escrita de modo a converter as instruções para código de máquina.

<img src="../images/sessao_02_1.png">

O JavaScript é amplamente categorizado como uma linguagem de criação de scripts ou uma linguagem interpretada.

### Javascript do lado cliente

O termo JavaScript do lado do cliente refere-se à maneira como o JavaScript funciona em seu navegador. Nesse caso, o 
mecanismo JavaScript está integrado ao código do navegador.

### Javascript do lado do servidor

O termo JavaScript do lado do servidor se refere ao uso da linguagem de codificação na lógica de back-end do servidor. 
Nesse caso, o mecanismo JavaScript está diretamente no servidor.

<img src="../images/sessao_02_02.png">


### Sintaxes e comandos basicos  da linguagem

Toda linguagem de programação precisa de uma padronização para reger as regras e o nivelamento da linguagem ao nível global, 
e para o JavaScript é isso que é o ECMAScript, a versão oficial da linguagem, tanto que o nome **JavaScript**, na verdade, é
uma tradição do mercado de desenvolvimento, sendo o nome oficial da linguagem **ECMAScript**.


* No JavaScript, instruções são chamadas de [**declaração**](https://developer.mozilla.org/pt-BR/docs/Glossary/Statement) e são separadas por um ponto e vírgula **(;)**
* JavaScript é **case-sensitive** (*Ou seja significa que caracteres em **caixa alta** e em **caixa baixa** são tratados de modo diferente*) 

* Uma **declaração** é uma linha de código que dá comando para execução de uma tarefa.


### Declarando variaveis

> **[Referência MDN](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Guide/Grammar_and_types)**

Você pode declarar uma variável de três formas:

- Com a palavra chave `[var]`. Por exemplo, var `x = 42`. Esta sintaxe pode ser usada para declarar tanto variáveis locais como variáveis globais.
- Por simples adição de valor. Por exemplo, `x = 42`. Isso declara uma variável global. Essa declaração gera um aviso de advertência no JavaScript. Você não deve usar essa variante.
- Com a palavra chave `[let]`. Por exemplo, `let y = 13`. Essa sintaxe pode ser usada para declarar uma variável local de escopo de bloco. 


> Convenções de escrita

> - Variaveis devem ser escritas com o padrão **c**amel**C**ase
> exemplo:

> ```var oneVariable = 12```

> - Constantes devem ser escritas em caixa alta para melhorar a legibilidade do codigo 
> exemplo:

> ```const PERCENTAGE = 0.33```


### Escopo de variável

Quando você declara uma váriavel fora de qualquer função, ela é chamada de variável global, porque está disponível
para qualquer outro código no documento atual. Quando você declara uma variável dentro de uma função, é chamada de 
variável local, pois ela está disponível somente dentro dessa função.

Utilização da sintaxe do var para declaração de escopo global


``` js linenums="1" hl_lines="2"
if (true) {
  var x = 5;
}
console.log(x); // 5

```

Utilização da sintaxe do var para declaração de escopo local

``` js linenums="1" hl_lines="2"

if (true) {
  let y = 5;
}
console.log(y); // ReferenceError: y não está definido

```

### Tipos de dados

- **String:** pode ser qualquer valor que esteja entre aspas simples ou aspas duplas e que, 
normalmente, representam textos em geral. Podem ser letras, números e sinais de pontuação;
- **Numérico:** números;
- **Symbol:** símbolos;
- **Booleano:** dados que apresentam apenas duas possibilidades de valores – true (verdadeiro)
ou false (falso);
- **Null e undefined:** são dados que representam variáveis que, ou não possuem valor (null) ou,
então, estão incompletas (undefined, ou seja, indefinidas);
- **Objeto**: tipo de dado que funciona como uma entidade independente, no qual há um conjunto de 
atributos aninhados a uma variável.

JavaScript é uma linguagem dinamicamente tipada. Isso significa que você não precisa especificar o
tipo de dado de uma variável quando declará-la, e tipos de dados são convertidos automaticamente conforme
a necessidade durante a execução do script.

``` js linenums="1"
var oneVariable = null // empty variable

oneVariable = 1 // number
oneVariable = "2" // string
oneVariable = "foo" // string
oneVariable = ["foo", "bar"] //array 
oneVariable = true //bolean 
oneVariable = {
	"field" : "value"
} // object

```

Em expressões envolvendo valores numérico e string com o operador `+`, O JavaScript converte valores numérico para
strings. Por exemplo, considere a seguinte declaração:

```js linenums="1"
 
x = "answer" + 42; // answer 42"
y = 42 + "answer"; // "42 is the answer"

```

Podemos verificar o tipo de dado através de um operador reservado do ecmascript chamado `typeof`

```js linenums="1"
var oneVariable = null // empty variable
typeof oneVariable // object

oneVariable = 1 // number
typeof oneVariable // number

```

### Convertendo tipos de dados

Quando estamos falando de números, podemos utilizar expressões para realizar a conversão de dados
do tipo string em outros formatos como numérico e ponto flutuante.

``` js linenums="1"
// ------------ expression parseInt ----------//
var oneVariable = "1" // string
console.log(typeof(oneVariable)) // string 

oneVariable = parseInt(oneVariable) 
console.log(typeof(oneVariable)) // number 

//-------------- expression parseFloat -----------//
var oneVariable = "1.10" // string
console.log(typeof(oneVariable)) // string 

oneVariable = parseFloat(oneVariable) 
console.log(typeof(oneVariable)) // float 

```
