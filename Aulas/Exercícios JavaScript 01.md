**Exercício 01 — Apresentação pessoal**

Objetivo: praticar variáveis, tipos de dados e exibição de informações no console.

Enunciado: crie um programa JavaScript que armazene as informações de um aluno e apresente os dados no console.

Dados a armazenar: Nome do aluno, Idade, Curso, Semestre atual

Requisitos:

Utilize let ou const para declarar as variáveis. Utilize o padrão camelCase nos nomes das variáveis. Utilize console.log() para exibir as informações. Apresente cada informação em uma linha separada.

Exemplo de resultado esperado:

Nome: Carlos

Idade: 20

Curso: Sistemas de Informação

Semestre: 3

Resultado:

const nome = "Carlos";

const idade = "20";

const curso = "Sistemas de Informação";

const semestre = "3";

**Resultado em Interpolação:**

console.log (`Nome: ${nome}, Idade: ${idade}, Curso: ${curso}, Semestre: ${semestre}`)

OU 

**Resultado em Concatenação:**

console.log ("Nome:" + nome + ", Idade: " + idade + ", Curso: " + curso + ", Semestre: " + semestre);

---

**Exercício 02 — Calculadora de compras**

Objetivo: praticar variáveis e operadores matemáticos.

Enunciado: uma loja vende cadernos por R$ 25,00 cada. Crie um programa que armazene o preço unitário e a quantidade comprada e calcule o valor total da compra.

Requisitos:

Crie uma variável para armazenar o preço unitário do caderno.

Crie uma variável para armazenar a quantidade comprada.

Calcule o valor total utilizando o operador de multiplicação *.

Exiba o preço unitário, a quantidade e o valor total no console.

Exemplo de resultado esperado:

Preço unitário: R$ 25

Quantidade: 4

Total da compra: R$ 100

**Resultado:**

preco = 25;

let QtdComprada = prompt("Quantos cadernos foram comprados?");

valor = preco * QtdComprada;

console.log ("O preço unitário é: " + preco + ", a quantidade adquira foram " + QtdComprada + ", o valor total se somou a " + valor + " reais."

---

Exercício 3 — Calculando a média do aluno

Objetivo: praticar variáveis numéricas, operações matemáticas e precedência de operadores.

Enunciado: um professor precisa calcular a média de um aluno que realizou três avaliações. Desenvolva um programa que armazene as notas e calcule a média aritmética simples.

Requisitos:

Crie três variáveis para armazenar as notas.

Calcule a média somando as três notas e dividindo o resultado por 3.

Utilize parênteses para estruturar a precedência da expressão matemática.

Exiba as três notas e a média final no console.

Exemplo de resultado esperado:

Nota 1: 8
Nota 2: 7
Nota 3: 9
Média final: 8

