**1) Escreva um programa em C que leia 3 números e apresente o maior.**

---

**2) Escreva um programa em C que leia o salario de um trabalhador e o valor da prestação de um empréstimo.**

**Se a prestação for maior que 20% do salário imprima: "Empréstimo não concedido, caso contrario imprima:  "Empréstimo concedido."**

primeiro: Selecione o tipo de variável

Segundo: Selecione o nome da variável.

#include <stdio.h>

{

//Tipo e nome da variável
  
  float salario, prestacao;

//Entrada do salário

  printf("Informe o seu salário: ");
  scanf("%f", &salario);
  printf("Informe o valor da prestação: ");
  scanf("%f",&prestacao);

//Fizemos a entrada, criamos agora o processamento.
 
  float LimiteParcela = (salario * (0,20);
if (prestacao>LimiteParcela)
  printf("Empréstimo não autorizado!!!");
  else printf("Empréstimo autorizado!!!");

  return 0;
}

---

**3)  Faça um programa que receba a altura e o sexo de uma pessoa e calcule e mostre seu peso ideal, utilizando as seguintes formulas (onde  h corresponde a altura):**

**• Homens: (72.7 ∗ h) − 58**

**• Mulheres: (62, 1 ∗ h) − 44, 7**

#include <stdio.h>

int main()

{
// Declare as variáveis:
 
  float altura, pesoIdeal;
  char sexo;

//Entrada de dados:

  printf("Sistema de Cálculo de Peso Ideal \n");
  printf ("Informe a sua altura: ");
  scanf("%f", &altura);
  printf("Informe o sexo: ");
  scanf(" %c",&sexo);

  //Cálculo do peso Ideal
  if (sexo =='M')
    PesoIdeal = (72.7 * altura) - 58;

  else if (sexo =='F')
    PesoIdeal = (62,1 * altura) - 44,7;

  //Apresentamos o resultado:

  printf("O peso ideal é %.2f", PesoIdeal);

  

  return 0;
}

**O % se torna um especificador da variável.**
