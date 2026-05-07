# atividade-estacionamentoEC

#include <stdio.h>

int main() {

    char placa[10];
    int tipo;
    float tempo;
    float valorHora = 0;
    float valorBase = 0;
    float desconto = 0;
    float multa = 0;
    float valorFinal = 0;

    // Entrada de dados
    printf("Digite a placa do veiculo: ");
    scanf("%s", placa);

    printf("Tipo do veiculo:\n");
    printf("1 - Carro\n2 - Moto\n3 - Caminhonete\n");
    scanf("%d", &tipo);

    printf("Digite o tempo de permanencia (em horas): ");
    scanf("%f", &tempo);

    // Definindo valor por hora
    switch(tipo) {
        case 1:
            valorHora = 5;
            break;
        case 2:
            valorHora = 3;
            break;
        case 3:
            valorHora = 8;
            break;
        default:
            printf("Tipo invalido!\n");
            return 0;
    }

    // Cálculo do valor base
    if(tempo <= 1) {
        valorBase = valorHora;
    } else {
        valorBase = tempo * valorHora;
    }

    // Aplicação de desconto
    if(tempo > 5) {
        desconto = valorBase * 0.10;
    }

    // Aplicação de multa
    if(tempo > 10) {
        multa = 20;
    }

    // Cálculo final
    valorFinal = valorBase - desconto + multa;

    // Saída
    printf("\n===== RESUMO =====\n");
    printf("Placa: %s\n", placa);

    printf("Tipo: ");
    if(tipo == 1) printf("Carro\n");
    else if(tipo == 2) printf("Moto\n");
    else printf("Caminhonete\n");

    printf("Tempo: %.2f horas\n", tempo);
    printf("Valor Base: R$ %.2f\n", valorBase);
    printf("Desconto: R$ %.2f\n", desconto);
    printf("Multa: R$ %.2f\n", multa);
    printf("Valor Final: R$ %.2f\n", valorFinal);

    return 0;
}