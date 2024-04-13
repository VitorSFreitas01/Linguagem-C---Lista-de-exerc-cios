# Linguagem-C---Lista-de-exerc-cios-While

#include <stdio.h>

int main() {
    int i;

    printf("Números de 1 até 10:\n");
    for (i = 1; i <= 10; i++) {
        printf("%d ", i);
    }
    printf("\n");

    return 0;
}
---------------------------------------------

#include <stdio.h>

int main() {
    int idade, contador = 0;
    
    printf("Digite a idade de 5 pessoas:\n");

    for (int i = 0; i < 5; i++) {
        printf("Pessoa %d: ", i + 1);
        scanf("%d", &idade);

        if (idade > 18) {
            contador++;
        }
    }

    printf("O número de pessoas com mais de 18 anos é: %d\n", contador);

    return 0;
}
---------------------------------------------

#include <stdio.h>

int main() {
    int numero;

    // Solicita ao usuário que digite um número válido entre 1 e 10
    printf("Digite um número entre 1 e 10: ");
    scanf("%d", &numero);

    // Verifica se o número está dentro do intervalo válido
    while (numero < 1 || numero > 10) {
        printf("Número inválido. Digite um número entre 1 e 10: ");
        scanf("%d", &numero);
    }

    // Calcula e imprime a tabuada do número
    int i = 1;
    while (i <= 10) {
        printf("%d X %d = %d\n", numero, i, numero * i);
        i++;
    }

    return 0;
}
----------------------------------------------
#include <stdio.h>

int main() {
    // Array de strings contendo os nomes dos meses
    char *meses[] = {"janeiro", "fevereiro", "março", "abril", "maio", "junho",
                     "julho", "agosto", "setembro", "outubro", "novembro", "dezembro"};

    // Imprime o número e o nome do mês
    for (int i = 0; i < 12; i++) {
        printf("%d - %s\n", i + 1, meses[i]);
    }

    return 0;
}
-------------------------------------------------

#include <stdio.h>

int main() {
    int senhaCorreta[4] = {1, 2, 3, 4}; // Senha correta
    int senhaDigitada[4]; // Senha digitada pelo usuário

    printf("Digite a senha (4 números inteiros separados por espaço): ");

    // Lê a senha digitada pelo usuário
    scanf("%d %d %d %d", &senhaDigitada[0], &senhaDigitada[1], &senhaDigitada[2], &senhaDigitada[3]);

    // Verifica se a senha está correta
    while (senhaDigitada[0] != senhaCorreta[0] || senhaDigitada[1] != senhaCorreta[1] ||
           senhaDigitada[2] != senhaCorreta[2] || senhaDigitada[3] != senhaCorreta[3]) {
        printf("Senha incorreta. Tente novamente: ");
        scanf("%d %d %d %d", &senhaDigitada[0], &senhaDigitada[1], &senhaDigitada[2], &senhaDigitada[3]);
    }

    printf("Senha correta.\n");

    return 0;
}
-----------------------------------------------

# Linguagem-C---Lista-de-exerc-cios-Swith-Case

#include <stdio.h>

int main() {
    int numero;

    // Solicita ao usuário que digite um número inteiro positivo
    printf("Digite um número inteiro positivo: ");
    scanf("%d", &numero);

    // Verifica se o número é positivo
    if (numero > 0) {
        // Verifica se o número é par ou ímpar usando o operador módulo (%)
        if (numero % 2 == 0) {
            printf("O número %d é par.\n", numero);
        } else {
            printf("O número %d é ímpar.\n", numero);
        }
    } else {
        printf("O número digitado não é positivo.\n");
    }

    return 0;
}
--------------------------------------------------

#include <stdio.h>

int main() {
    char letra;

    // Solicita ao usuário que digite uma letra
    printf("Digite uma letra minúscula: ");
    scanf(" %c", &letra);

    // Verifica se a letra é uma vogal
    if (letra == 'a' || letra == 'e' || letra == 'i' || letra == 'o' || letra == 'u') {
        printf("A letra %c é uma vogal.\n", letra);
    }
    // Verifica se a letra é uma consoante (considerando apenas letras minúsculas)
    else if ((letra >= 'a' && letra <= 'z') && !(letra == 'a' || letra == 'e' || letra == 'i' || letra == 'o' || letra == 'u')) {
        printf("A letra %c é uma consoante.\n", letra);
    }
    // Se não for uma letra minúscula
    else {
        printf("Por favor, digite uma letra minúscula.\n");
    }

    return 0;
}
----------------------------------------------------

#include <stdio.h>

int main() {
    int mes;

    // Solicita ao usuário que digite o número do mês
    printf("Digite o número do mês (1 a 12): ");
    scanf("%d", &mes);

    // Verifica o número de dias baseado no mês
    switch (mes) {
        case 2:
            printf("O mês de fevereiro tem 28 dias.\n");
            break;
        case 4:
        case 6:
        case 9:
        case 11:
            printf("O mês tem 30 dias.\n");
            break;
        default:
            printf("O mês tem 31 dias.\n");
            break;
    }

    return 0;
}

