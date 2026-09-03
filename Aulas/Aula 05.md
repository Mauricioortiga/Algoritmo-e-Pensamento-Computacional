1) Faça um programa em C para uma loja de tintas. O programa deverá pedir o tamanho em metros quadrados da área a ser pintada.

Considere que a cobertura da tinta é de 1 litro para cada 3 metros quadrados e que a tinta é vendida em latas de 18 litros, que custam R$ 80,00.

Informe ao usuário a quantidades de latas de tinta a serem compradas e o preço total.

#include <stdio.h>

int main()
{
float largura;
float comprimento;
float metroquadrado;
float cobertura;
int latas;

printf ("Informe a largura da parede em Metros: ");
scanf ("%f", &largura);
printf ("Informe o comprimento da parede em Metros: ");
scanf ("%f", &comprimento);

metroquadrado = comprimento * largura;

cobertura = metroquadrado / 3;

latas = cobertura / 18;

printf ("O metro quadrado é %.1f", metroquadrado);
printf (" m²");
printf ("\n Será utilizado %.2f", cobertura); 

printf(" litros de tinta para cobrir a área.");

printf ("\n Foi utilizado %d", latas);
printf (" latas de tinta");

return 0;
    
}

2) Um posto está vendendo combustíveis com a seguinte tabela de descontos: Álcool: até 20 litros, desconto de 3% por litro acima de 20 litros, desconto de 5% por litro Gasolina: até 20 litros, desconto de 4% por litro acima de 20 litros, desconto de 6% por litro.



3) Escreva um programa C que leia o número de litros vendidos, o tipo de combustível (codificado da seguinte forma: A-álcool, G-gasolina), calcule e imprima o valor a ser pago pelo cliente sabendo-se que o preço do litro da gasolina é R$ 2,50 o preço do litro do álcool é R$ 1,90.
