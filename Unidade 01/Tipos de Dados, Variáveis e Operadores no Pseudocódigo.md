🔨 **Neste conteúdo, iremos:**

• Identificar os tipos de dados mais comuns

• Declarar e utilizar variáveis no pseudocódigo

• Criar entradas e saídas com clareza

• Utilizar operadores aritméticos, relacionais e lógicos

• Aplicar esses conceitos para resolver uma situação-problema simples

---

🔨 **Situação-Problema:**

📜 **Um sistema precisa verificar se um aluno foi aprovado.**

Para isso, ele deve:

• Receber duas notas.

• Calcular a média.

• Mostrar se o aluno está aprovado ou reprovado.

⚡**Como iremos estruturar esse raciocínio em pseudocódigo?**

---

🔨 **Identifique os tipos de dados:**

**Inteiro:**

Numeros sem casas decimais.

**Real:** 

Números com casas decimais.

**Caractere:** 

Letras ou símbolos (Ex: 'A', '$')

**Lógico:** 

Verdadeiro ou falso (booleano)

**Literal:** 

**Sequência de caracteres:**

(ex: "Olá Mundo")

---

🔨 **Declare uma variável:**

**Variáveis:** 

São espaços de memória com nome. Devem ser declaradas antes do uso.

Exemplo: 

real nota1, nota2

real media

---

• **Nome claro**= código **mais legível!**

• **Não use nomes que sejam palavras reservadas do código!**

---

🔨 **Com a variável declarada e o tipo definido, definimos a entrada e saída:**

**Entrada:** 

Permite ler dados do usuário

-> leia(nota1)

**Saída:** 

Exibe mensagens ou resultados

-> escreva("Sua média é: ", media)

---

🔨**Com a entrada e a saída definida, descrevemos os valores:**

**Operadores aritméticos:**

Soma +

Subtração -

Multiplicação *

Divisão /

Exemplo:

media <- (nota1 + nota2) /2

• **A seta virada para media está recebendo o resultado.**

---

🔨 **Operadores relacionais:**

Igual =

Diferente <>

Menor que >

Menor ou igual <=

Maior que >

Maior ou igual >=

---

🔨 **Operadores lógicos:**

Conjunção E

Disjunção OU

Negação NÃO

Exemplo:

se (media >= 7) E (frequencia >= 75) então
  escreva ("Aprovado")

---

🔨 **Situação-Problema:**

algoritmo "VerificaAprovacao"
var 
  real nota1, nota2, media
inicio
  leia (nota1)
  leia (nota2)
  media <- (nota1 + nota2) /2

  se media >= 7 então
    escreva ("Aprovado")
  senao
    escreva ("Reprovado")
  fimalgoritmo




