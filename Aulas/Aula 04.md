Lista de Exercícios II - Fundamentos da Linguagem C 



**1) O valor pago por um Hotel da Praia de Iracema para seus porteiros é de R$ 10,25 por hora de trabalho. Faça um programa que pergunte ao usuário quantas horas ele trabalhou e imprima na tela o valor do salário a ser recebido por ele.**

#include <stdio.h>

int main()

{

float salario, horas;

printf ("Informe a quantidade de horas trabalhadas");

scanf ("%f", &horas);

salario = (horas * 10.25);

printf ("O seu salário será de %.2f", salario);

return 0;

}

---

2) Sabendo que na Faculdade ABC a média mínima é 7,0 e a tolerância de faltas é 15 % da carga horária do curso, faça um programação em C que peça as informações necessárias e informe a situação do usuário.

#include <stdio.h>

int main()

{

float nota1, nota2, media, cargahoraria, faltas, limitefaltas, verificacao

printf ("Informe a primeira nota adquirida: ");
scanf ("%f", &nota1);

printf ("Informe a segunda nota adquirida: ");
scanf ("%f", &nota2);

printf ("Informe a carga horária do seu curso: ");
scanf ("%f", &cargahoraria);

printf ("Informe o número de faltas: ");
scanf ("%d", &faltas);

media = (nota1+nota2) /2;
printf ("A média será de %.2f", media);

limitefaltas = cargahoraria * 0.15;

verificacao = cargahoraria / faltas;

if (media >=7.0 && verificacao <= limitefaltas) {
printf ("Situação do curso: APROVADO."); 
    
}else printf ("Situação do curso: REPROVADO.");

return 0;

}

**CORREÇÃO:**

#include <stdio.h>

int main ()
{
  float media, cargaHoraria, faltas, percentualFaltas;
  printf ("Sistema Acadêmico\n");

  printf ("Informe a média do aluno: ");
  scanf ("%f, &media);

  printf ("Informe a carga horária (número de aulas): ");
  scanf ("%%f" ,&cargaHoraria);

  printf ("Informe o número de faltas: ");
  scanf ("%f", &faltas);  

  percentualFaltas = (faltas / cargaHoraria) * 100;
  printf ("\n --- Resultado --- \n");
  printf ("Média: %f", media);
  printf ("Percentual de faltas: %.2f",percentualFaltas);

  if (media) >= 7.0 && percentualFaltas <= 15.0)
    printf ("Situação: APROVADO \n);
  else printf ("Situação: Reprovado \n);
  
  return 0;

}
