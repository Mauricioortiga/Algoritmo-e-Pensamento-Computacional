Todo algoritmo é processado em entrada, processamento e saída.

**3. Construa uma programação em C que peça o nome, endereço, sexo, cidade, estado, idade dos funcionários.
Além disto, dado o Salário Bruto do funcionário, calcule o seu Salário Líquido. Considere que os descontos podem ser o Vale Transporte(2%), Vale Alimentação(5%) e Plano de Saúde(10%).**

#include <stdio.h>

int main ()
{

//Declaração das variáveis: Char é o tipo caractere, nome é a variável e 100 é o limite de caracteres.
 
  char nome[100];
  char endereco[150];
  char sexo;
  char cidade[50];
  char estado[50];
  int idade;
  float salarioBruto, salarioLiquido, valeTransporte, valeAlimentacao, planodeSaude;

  printf("**** Sistema de Cálculo de Salário ****")
  printf("Nome......: ");
  
  //% declara o tipo de variável, ^ é uma estrutura de array, sendo utilizado para uma estrutura de dados onde temos vários elementos, sendo definido por colchete [50] na declaração.


  //PARA O CHAR, É IMPORTANTE HAVER O ESPAÇO LOGO APOS "", SENÃO IRÁ DAR ERRO!!!
  
  //CAPTURA DAS INFORMAÇÕES:
  
  printf("Nome......: ");
  scanf(" %[^\n],nome);
  
  printf("Endereço......: ");
  scanf(" %[^\n]",endereco);
  
  printf("Cidade......: ");
  scanf(" %[^\n]",cidade);
  
  printf("estado......: ");
  scanf(" %[^\n]",estado);
  
  printf("Sexo......: ");
  scanf("%c",&sexo);
  
  printf("Idade......: ");
  scanf("%d",&idade);
  
  printf("Salário bruto......: ");
  scanf("%f",f&salarioBruto);

  // Processamento:

  valeTransporte = salarioBruto * 0.02;
  valeAlimentacao = salarioBruto * 0.05;
  planodeSaude = salarioBruto * 0.10;
  salarioLiquido = salarioBruto - valeTransporte - valeAlimentacao - planodeSaude;

  // Imprimindo o resultado:
  
  printf("\n**** Salário Líquido ......: ");
  printf("\nNome...: %s\n", nome);
  printf("\nSalário bruto...: R$ %.2f", salarioBruto);
  printf("\n(-) Vale Transporte...: R$ %.2f", valeTransporte);
  printf("\n(-) Vale Alimentação...: R$ %.2f", valeAlimentacao);
  printf("\n(-) Plano de Saúde...: R$ %.2f", planodeSaude);
  printf("\n(-) Salário Líquido...: R$ %.2f", salarioLiquido);
  
  return 0;
  
  
