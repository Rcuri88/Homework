#include <stdio.h>

int main() {
    int num1, num2, num3;
    
    // Solicitar ao usuário três números inteiros
    printf("=== PROGRAMA DE OPERADORES ARITMÉTICOS, RELACIONAIS E LÓGICOS ===\n\n");
    printf("Digite o primeiro número inteiro: ");
    scanf("%d", &num1);
    
    printf("Digite o segundo número inteiro: ");
    scanf("%d", &num2);
    
    printf("Digite o terceiro número inteiro: ");
    scanf("%d", &num3);
    
    printf("\n--- OPERAÇÕES ARITMÉTICAS ---\n");
    
    // 1. Operações Aritméticas
    printf("Soma: %d + %d + %d = %d\n", num1, num2, num3, num1 + num2 + num3);
    printf("Subtração: %d - %d - %d = %d\n", num1, num2, num3, num1 - num2 - num3);
    printf("Multiplicação: %d * %d * %d = %d\n", num1, num2, num3, num1 * num2 * num3);
    
    // Verificar divisão por zero
    if (num2 != 0 && num3 != 0) {
        printf("Divisão: %d / %d / %d = %d\n", num1, num2, num3, num1 / num2 / num3);
    } else {
        printf("Divisão: Não é possível dividir por zero\n");
    }
    
    printf("\n--- OPERADORES RELACIONAIS ---\n");
    
    // 2. Operadores Relacionais
    printf("Primeiro número (%d) é maior que o segundo (%d)? ", num1, num2);
    if (num1 > num2) {
        printf("SIM (verdadeiro)\n");
    } else {
        printf("NÃO (falso)\n");
    }
    
    printf("Segundo número (%d) é menor que o terceiro (%d)? ", num2, num3);
    if (num2 < num3) {
        printf("SIM (verdadeiro)\n");
    } else {
        printf("NÃO (falso)\n");
    }
    
    printf("\n--- OPERADORES LÓGICOS ---\n");
    
    // 3. Operadores Lógicos
    int primeiro_positivo = (num1 > 0);      // Verifica se o primeiro é positivo
    int segundo_par = (num2 % 2 == 0);       // Verifica se o segundo é par
    
    printf("Primeiro número (%d) é positivo? %s\n", num1, primeiro_positivo ? "SIM" : "NÃO");
    printf("Segundo número (%d) é par? %s\n", num2, segundo_par ? "SIM" : "NÃO");
    
    // Verificar se AMBAS as condições são verdadeiras
    if (primeiro_positivo && segundo_par) {
        printf("\n✓ MENSAGEM ESPECIAL: O primeiro número é positivo E o segundo número é par!\n");
    } else {
        printf("\nAs condições de ser positivo (primeiro) e par (segundo) não foram ambas atendidas.\n");
    }
    
    printf("\n=== FIM DO PROGRAMA ===\n");
    
    return 0;
}
