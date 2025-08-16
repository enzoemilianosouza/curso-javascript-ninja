# Desafio da semana #2

Nesse exercício, você está livre para escolher os nomes para suas variáveis e funções! :smile:

```js
// Crie uma função que receba dois argumentos e retorne a soma dos mesmos.
function somaParametro(x, y) {
  return x + y;
}

// Declare uma variável que receba a invocação da função criada acima, passando dois números quaisquer por argumento, e somando `5` ao resultado retornado da função.
const recebeFunction = somaParametro(5, 5) + 5;

// Qual o valor atualizado dessa variável?
15;

// Declare uma nova variável, sem valor.
var semValor;

/*
Crie uma função que adicione um valor à variável criada acima, e retorne a string:
    O valor da variável agora é VALOR.
Onde VALOR é o novo valor da variável.
*/

function addValorVar(valor) {
  semValor = valor;

  return "o valor da variavel agora é:" + semValor;
}

/////////////////////////////////////////////////////////////////////////////////////////////////////////
// correção: ele não pediu param, então deveria ficar:
function addValor() {
  var valor = 25;
  return "o valor da variavel agora é:" + valor;
}

addValor(); // aqui estou chamando a função e quando chamo, ela atribui a var valor o numero 25 e retorna a mensagem.

/////////////////////////////////////////////////////////////////////////////////////////////////////////

// Invoque a função criada acima.
addValorVar();

// Qual o retorno da função? (Use comentários de bloco).
/* 'o valor da variavel agora éundefined' /*


/*
Crie uma função com as seguintes características:
1. A função deve receber 3 argumentos;
2. Se qualquer um dos três argumentos não estiverem preenchidos, a função deve retornar a string:
    Preencha todos os valores corretamente!
3. O retorno da função deve ser a multiplicação dos 3 argumentos, somando `2` ao resultado da multiplicação.
*/

function verificaParams(x, y, z) {
  if (x === undefined || y === undefined || z === undefined) {
    // quando não é passado nenhum valor para um var, ela é undefined. correto! > null é um valor 
    return "Preencha todos os valores corretamente!";
  }

  var multiplicaParams = x * y * z;

  return multiplicaParams + 2;
}

// Invoque a função criada acima, passando só dois números como argumento.

verificaParams(5, 5);

// Qual o resultado da invocação acima? (Use comentários para mostrar o valor retornado).

// 'Preencha todos os valores corretamente!'

// Agora invoque novamente a função criada acima, mas passando todos os três argumentos necessários.

verificaParams(5, 5, 5);
// Qual o resultado da invocação acima? (Use comentários para mostrar o valor retornado).

// 127

/*
Crie uma função com as seguintes características:
1. A função deve receber 3 argumentos.
2. Se somente um argumento for passado, retorne o valor do argumento.
3. Se dois argumentos forem passados, retorne a soma dos dois argumentos.
4. Se todos os argumentos forem passados, retorne a soma do primeiro com o segundo, e o resultado, dividido pelo terceiro.
5. Se nenhum argumento for passado, retorne o valor booleano `false`.
6. E ainda, se nenhuma das condições acima forem atendidas, retorne `null`.
*/

function tresArgumentos(x, y, z) {
  if (x && y && z) {
    return (x + y) / z;
  } else if (x && y) {
    return x + y;
  } else if (!x && !y && !z) {
    return false;
  } else if (x) {
    return x;
  } else {
    return null;
  }
}

// Invoque a função acima utilizando todas as possibilidades (com nenhum argumento, com um, com dois e com três.) Coloque um comentário de linha ao lado da função com o resultado de cada invocação.

tresArgumentos(); // false
tresArgumentos(5); // 5
tresArgumentos(5, 10); // 15
tresArgumentos(5, 10, 15); // 1
```
