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

3. Construa um programação em C que peça o Nome, Endereço, Sexo, Cidade, Estado, Idade dos funcionários. Além disto, dado o Salário Bruto do funcionário, calcule o seu Salário Líquido. Considere que os descontos podem ser o Vale Transporte (2%), Vale Alimentação (5%) e Plano de Saúde (10%).

#include <stdio.h>

int main() 
{
    // Declaração das variáveis
    char nome[50];
    char endereco[50];
    char sexo;
    char cidade[50];
    char estado[50];
    int idade;

    float salarioBruto;
    float valeTransporte;
    float valeAlimentacao;
    float planoSaude;
    float totalDescontos;
    float salarioLiquido;

    printf("=== CADASTRO DE FUNCIONARIO ===\n");

    // Leitura dos dados utilizando & em todas as variaveis
    printf("Informe o primeiro nome: ");
    scanf("%s", &nome);

    printf("Informe o endereco (uma palavra ou sem espacos): ");
    scanf("%s", &endereco);

    printf("Informe a cidade: ");
    scanf("%s", &cidade);

    printf("Informe o estado (sigla EX: DF): ");
    scanf("%s", &estado);

    printf("Informe o sexo (M/F): ");
    scanf(" %c", &sexo);

    printf("Informe a idade: ");
    scanf("%d", &idade);

    printf("Informe o salario bruto: ");
    scanf("%f", &salarioBruto);

    // Calculo dos descontos passo a passo
    valeTransporte = salarioBruto * 0.02;
    valeAlimentacao = salarioBruto * 0.05;
    planoSaude = salarioBruto * 0.10;

    totalDescontos = valeTransporte + valeAlimentacao + planoSaude;
    salarioLiquido = salarioBruto - totalDescontos;

    // Exibicao dos resultados
    printf("\n--- RESULTADO ---\n");
    printf("Nome: %s\n", nome);
    printf("Endereco: %s\n", endereco);
    printf("Cidade: %s\n", cidade);
    printf("Estado: %s\n", estado);
    printf("Sexo: %c\n", sexo);
    printf("Idade: %d anos\n", idade);

    printf("\nSalario Bruto: R$ %.2f\n", salarioBruto);
    printf("Desconto Vale Transporte: R$ %.2f\n", valeTransporte);
    printf("Desconto Vale Alimentacao: R$ %.2f\n", valeAlimentacao);
    printf("Desconto Plano de Saude: R$ %.2f\n", planoSaude);
    printf("Total de Descontos: R$ %.2f\n", totalDescontos);
    printf("Salario Liquido: R$ %.2f\n", salarioLiquido);

    return 0;
}
