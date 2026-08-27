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

float nota1, nota2, media, cargahoraria;

printf ("Informe a primeira nota adquirida: ");

scanf ("%f", &nota1);

printf ("Informe a segunda nota adquirida: ");

scanf ("%f", &nota2);

printf ("Informe a carga horária do seu curso: ");

scanf ("%f", &cargahoraria);

if (cargahoraria )

media = (nota1+nota2/2);

printf ("A média será de %.2f", media);

return 0;

}

**CORREÇÃO:**

3) Construa um programação em C que peça o Nome, Endereço, Sexo, Cidade, Estado, Idade dos funcionários. Além disto, dado o Salário Bruto do funcionário, calcule o seu Salário Líquido. Considere que os descontos podem ser o Vale Transporte (2%), Vale Alimentação (5%) e Plano de Saúde (10%).
