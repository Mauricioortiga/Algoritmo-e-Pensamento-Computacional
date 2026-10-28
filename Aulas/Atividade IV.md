**EXERCÍCIO 1 — MONITORAMENTO DE ABASTECIMENTO:**

Uma transportadora deseja controlar o consumo de combustível de um caminhão durante 10 viagens. Para cada viagem, será registrada a quantidade de litros de combustível consumidos.

Desenvolva um programa em C que armazene os consumos em um vetor de números reais.

O programa deverá:

1. Ler o consumo de combustível das 10 viagens.

2. Calcular o consumo total de combustível.

3. Calcular o consumo médio por viagem.

4. Identificar a viagem com maior consumo e apresentar seu número e valor.

5. Contar quantas viagens tiveram consumo superior a 50 litros.

6. Exibir os consumos na ordem inversa àquela em que foram informados.

Requisitos técnicos:

- Utilize um vetor float consumo[10].

- Implemente a função calcularTotal() para retornar o consumo total.

- Implemente a função calcularMedia() para retornar o consumo médio.

- Implemente a função contarViagens() para retornar a quantidade de viagens com consumo superior a 50 litros.

- Utilize laços de repetição para leitura, processamento e exibição dos dados.

Critérios avaliados: vetores, acumuladores, comparação de valores, funções e percursos em ordem inversa.

**RESPOSTA EXERCÍCIO 01:**
#include <stdio.h>

float calcularTotal(float consumo[]) {
    float total = 0;
    for (int i = 0; i < 10; i++) {
        total = total + consumo[i];
    }
    return total;
}

float calcularMedia(float consumo[]) {
    return calcularTotal(consumo) / 10;
}

int contarViagens(float consumo[]) {
    int contador = 0;
    for (int i = 0; i < 10; i++) {
        if (consumo[i] > 50) {
            contador++;
        }
    }
    return contador;
}

int main() {
    float consumo[10];
    int i;

    for (i = 0; i < 10; i++) {
        printf("Consumo da viagem %d (litros): ", i + 1);
        scanf("%f", &consumo[i]);
    }

    float total = calcularTotal(consumo);
    float media = calcularMedia(consumo);
    int acima50 = contarViagens(consumo);

    float maior = consumo[0];
    int viagemMaior = 1;
    for (i = 1; i < 10; i++) {
        if (consumo[i] > maior) {
            maior = consumo[i];
            viagemMaior = i + 1;
        }
    }

    printf("\nConsumo total: %.2f litros\n", total);
    printf("Consumo medio por viagem: %.2f litros\n", media);
    printf("Viagem com maior consumo: %d (%.2f litros)\n", viagemMaior, maior);
    printf("Viagens com consumo superior a 50 litros: %d\n", acima50);

    printf("\nConsumos na ordem inversa:\n");
    for (i = 9; i >= 0; i--) {
        printf("Viagem %d: %.2f litros\n", i + 1, consumo[i]);
    }

    return 0;
}

---

**EXERCÍCIO 2 — ANÁLISE DE DESEMPENHO ACADÊMICO:**

Uma instituição de ensino deseja analisar o desempenho de uma turma com 12 alunos. Para simplificar o exercício, cada aluno receberá uma nota inteira entre 0 e 10.

Desenvolva um programa em C que armazene as notas em um vetor de números inteiros.

O programa deverá:

1. Ler e validar as notas dos 12 alunos, aceitando somente valores entre 0 e 10.

2. Calcular a média da turma.

3. Contar quantos alunos foram aprovados, considerando nota maior ou igual a 7.

4. Identificar a maior e a menor nota.

5. Contar quantos alunos obtiveram nota acima da média da turma.

6. Exibir todas as notas na ordem em que foram cadastradas.

Requisitos técnicos:

- Utilize um vetor int notas[12].

- Implemente a função calcularMedia() para retornar a média da turma.

- Implemente a função contarAprovados() para retornar o número de alunos aprovados.

- Implemente a função encontrarMaiorNota() para retornar a maior nota.

- Implemente a função contarAcimaMedia() para contar as notas superiores à média.

- Utilize laços de repetição e estruturas condicionais para processar os dados.

Regra importante: caso o usuário informe uma nota inválida, o programa deverá solicitar novamente a nota do mesmo aluno.

Critérios avaliados: validação de entradas, funções com parâmetros e retorno, média aritmética e contagem condicional.

**RESPOSTA EXERCÍCIO 02:**

#include <stdio.h>

float calcularMedia(int notas[]) {
    int soma = 0;
    for (int i = 0; i < 12; i++) {
        soma = soma + notas[i];
    }
    return soma / 12.0;
}

int contarAprovados(int notas[]) {
    int aprovados = 0;
    for (int i = 0; i < 12; i++) {
        if (notas[i] >= 7) {
            aprovados++;
        }
    }
    return aprovados;
}

int encontrarMaiorNota(int notas[]) {
    int maior = notas[0];
    for (int i = 1; i < 12; i++) {
        if (notas[i] > maior) {
            maior = notas[i];
        }
    }
    return maior;
}

int contarAcimaMedia(int notas[], float media) {
    int contador = 0;
    for (int i = 0; i < 12; i++) {
        if (notas[i] > media) {
            contador++;
        }
    }
    return contador;
}

int main() {
    int notas[12];
    int i;

    for (i = 0; i < 12; i++) {
        printf("Nota do aluno %d: ", i + 1);
        scanf("%d", &notas[i]);
        while (notas[i] < 0 || notas[i] > 10) {
            printf("Nota invalida! Digite novamente a nota do aluno %d: ", i + 1);
            scanf("%d", &notas[i]);
        }
    }

    float media = calcularMedia(notas);
    int aprovados = contarAprovados(notas);
    int maior = encontrarMaiorNota(notas);
    int acimaMedia = contarAcimaMedia(notas, media);

    int menor = notas[0];
    for (i = 1; i < 12; i++) {
        if (notas[i] < menor) {
            menor = notas[i];
        }
    }

    printf("\nMedia da turma: %.2f\n", media);
    printf("Alunos aprovados: %d\n", aprovados);
    printf("Maior nota: %d\n", maior);
    printf("Menor nota: %d\n", menor);
    printf("Alunos acima da media: %d\n", acimaMedia);

    printf("\nNotas cadastradas:\n");
    for (i = 0; i < 12; i++) {
        printf("Aluno %d: %d\n", i + 1, notas[i]);
    }

    return 0;
}

---

**EXERCÍCIO 3 — CONTROLE DE MOVIMENTAÇÃO DE ESTOQUE:**

Uma loja de equipamentos eletrônicos possui 10 produtos cadastrados. Cada posição de um vetor representa a quantidade disponível em estoque de um produto.

Desenvolva um programa em C que permita registrar as quantidades iniciais e, em seguida, realizar operações de entrada e saída de produtos.

O programa deverá:

1. Ler a quantidade inicial dos 10 produtos.

2. Exibir um menu com as opções: consultar estoque, registrar entrada, registrar saída e encerrar o programa.

3. Permitir que o usuário informe o número do produto e a quantidade movimentada.

4. Atualizar o estoque após cada operação.

5. Impedir saídas superiores à quantidade disponível e impedir quantidades negativas ou iguais a zero nas movimentações.

6. Ao consultar o estoque, exibir a quantidade de cada produto, o total de unidades armazenadas e quantos produtos estão sem estoque.

Requisitos técnicos:

- Utilize um vetor int estoque[10].

- Implemente a função exibirMenu() para apresentar as opções.

- Implemente a função registrarEntrada() para atualizar o estoque de um produto.

- Implemente a função registrarSaida() para validar e atualizar uma saída.

- Implemente a função calcularTotalEstoque() para retornar a soma das quantidades.

- Implemente a função contarProdutosZerados() para retornar a quantidade de produtos sem estoque.

- Utilize um laço de repetição para manter o menu ativo até que o usuário escolha encerrar.

**RESPOSTA EXERCÍCIO 03:

#include <stdio.h>

int exibirMenu() {
    int opcao;
    printf("\n1 - Consultar estoque\n");
    printf("2 - Registrar entrada\n");
    printf("3 - Registrar saida\n");
    printf("4 - Encerrar\n");
    printf("Opcao: ");
    scanf("%d", &opcao);
    return opcao;
}

int registrarEntrada(int estoque[], int produto, int quantidade) {
    estoque[produto - 1] = estoque[produto - 1] + quantidade;
    return estoque[produto - 1];
}

int registrarSaida(int estoque[], int produto, int quantidade) {
    if (quantidade > estoque[produto - 1]) {
        return 0;
    }
    estoque[produto - 1] = estoque[produto - 1] - quantidade;
    return 1;
}

int calcularTotalEstoque(int estoque[]) {
    int total = 0;
    for (int i = 0; i < 10; i++) {
        total = total + estoque[i];
    }
    return total;
}

int contarProdutosZerados(int estoque[]) {
    int zerados = 0;
    for (int i = 0; i < 10; i++) {
        if (estoque[i] == 0) {
            zerados++;
        }
    }
    return zerados;
}

int main() {
    int estoque[10];
    int i, opcao, produto, quantidade;

    for (i = 0; i < 10; i++) {
        printf("Quantidade inicial do produto %d: ", i + 1);
        scanf("%d", &estoque[i]);
    }

    do {
        opcao = exibirMenu();

        switch (opcao) {
            case 1:
                for (i = 0; i < 10; i++) {
                    printf("Produto %d: %d\n", i + 1, estoque[i]);
                }
                printf("Total de unidades: %d\n", calcularTotalEstoque(estoque));
                printf("Produtos sem estoque: %d\n", contarProdutosZerados(estoque));
                break;

            case 2:
                printf("Numero do produto (1 a 10): ");
                scanf("%d", &produto);
                if (produto < 1 || produto > 10) {
                    printf("Produto invalido!\n");
                } else {
                    printf("Quantidade de entrada: ");
                    scanf("%d", &quantidade);
                    if (quantidade <= 0) {
                        printf("Quantidade invalida!\n");
                    } else {
                        registrarEntrada(estoque, produto, quantidade);
                        printf("Entrada registrada.\n");
                    }
                }
                break;

            case 3:
                printf("Numero do produto (1 a 10): ");
                scanf("%d", &produto);
                if (produto < 1 || produto > 10) {
                    printf("Produto invalido!\n");
                } else {
                    printf("Quantidade de saida: ");
                    scanf("%d", &quantidade);
                    if (quantidade <= 0) {
                        printf("Quantidade invalida!\n");
                    } else if (registrarSaida(estoque, produto, quantidade) == 0) {
                        printf("Estoque insuficiente!\n");
                    } else {
                        printf("Saida registrada.\n");
                    }
                }
                break;

            case 4:
                printf("Programa encerrado.\n");
                break;

            default:
                printf("Opcao invalida!\n");
        }
    } while (opcao != 4);

    return 0;
}
