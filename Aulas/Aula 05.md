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
    int valorTotal;


    printf ("Informe a largura da parede em Metros: ");
    scanf ("%f", &largura);
    printf ("Informe o comprimento da parede em Metros: ");
    scanf ("%f", &comprimento);

    metroquadrado = comprimento * largura;

    cobertura = metroquadrado / 3;

    latas = cobertura / 18;

    valorTotal = latas * 80;

    printf ("O metro quadrado é %.1f", metroquadrado);
    printf (" m²");
    printf ("\n Será utilizado %.2f", cobertura); 

    printf(" litros de tinta para cobrir a área.");

    printf ("\n Foi utilizado %d", latas);
    printf (" latas de tinta");

    printf ("\n O valor ficou em R$ %d", valorTotal);
    printf (" reais.");

    return 0;
    
    }

2) Um posto está vendendo combustíveis com a seguinte tabela de descontos: 

Álcool: até 20 litros, desconto de 3% por litro; Acima de 20 litros, desconto de 5% por litro.

Gasolina: até 20 litros, desconto de 4% por litro; Acima de 20 litros, desconto de 6% por litro.

Escreva um programa C que leia o número de litros vendidos, o tipo de combustível (codificado da seguinte forma: A-álcool, G-gasolina), calcule e imprima o valor a ser pago pelo cliente sabendo-se que o preço do litro da gasolina é R$ 2,50 o preço do litro do álcool é R$ 1,90.


#include <stdio.h>

    int main() {
    float litros, preco_base, desconto, valor_com_desconto, total;
    char tipo;

    printf("Digite o numero de litros vendidos: ");
    scanf("%f", &litros);

    printf("Digite o tipo de combustivel (A-alcool, G-gasolina): ");
    scanf(" %c", &tipo);

    if (tipo == 'A' || tipo == 'a') {
        preco_base = 1.90;
        
        if (litros <= 20) {
            desconto = 0.03; // 3% de desconto
        } else {
            desconto = 0.05; // 5% de desconto
        }
        
        valor_com_desconto = preco_base * (1 - desconto);
        total = litros * valor_com_desconto;
        
        printf("\nCombustivel: Alcool\n");
        printf("Valor total a pagar: R$ %.2f\n", total);
    } 
    else if (tipo == 'G' || tipo == 'g') {
        preco_base = 2.50;
        
        if (litros <= 20) {
            desconto = 0.04; // 4% de desconto
        } else {
            desconto = 0.06; // 6% de desconto
        }
        
        valor_com_desconto = preco_base * (1 - desconto);
        total = litros * valor_com_desconto;
        
        printf("\nCombustivel: Gasolina\n");
        printf("Valor total a pagar: R$ %.2f\n", total);
    } 
    else {
        printf("\nTipo de combustivel invalido!\n");
    }

    return 0;
}

3) Faça um programa que leia uma quantidade de segundos e converta esse valor para:

horas;
minutos;
segundos.

#include <stdio.h>

    int main() {
    int total_segundos, horas, minutos, segundos;

    printf("Digite a quantidade de segundos: ");
    scanf("%d", &total_segundos);

    horas = total_segundos / 3600;
    
    int resto = total_segundos % 3600;
    
    minutos = resto / 60;
    
    segundos = resto % 60;

    printf("\nTempo formatado: %d hora(s), %d minuto(s) e %d segundo(s)\n", horas, minutos, segundos);

    return 0;
}
