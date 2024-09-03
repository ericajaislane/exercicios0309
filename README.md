# exercicios0309
1.	Escreva um algoritmo para ler 2 valores e se o segundo valor informado for ZERO, deve ser lido um novo valor, ou seja, para o segundo valor n˜ao pode ser aceito o valor zero e imprimir o resultado da divis˜ao do primeiro valor lido pelo segundo valor lido. (utilizar a estrutura while).
#include <stdio.h>
#include <locale.h>

int main() {
    setlocale(LC_ALL, "Portuguese");

    float valor1, valor2;

    printf("Digite o primeiro valor: ");
    scanf("%f", &valor1);

    printf("Digite o segundo valor (diferente de zero): ");
    scanf("%f", &valor2);

    while (valor2 == 0) {
        printf("Valor inválido. Digite um valor diferente de zero: ");
        scanf("%f", &valor2);
    }

    printf("Resultado da divisão: %.2f\n", valor1 / valor2);

    return 0;
}
2.	Reescreva o exerc´ıcio anterior utilizando a estrutura do...while.

#include <stdio.h>
#include <locale.h>

int main() {
    setlocale(LC_ALL, "Portuguese");

    float valor1, valor2;

    printf("Digite o primeiro valor: ");
    scanf("%f", &valor1);

    do {
        printf("Digite o segundo valor (diferente de zero): ");
        scanf("%f", &valor2);

        if (valor2 == 0) {
            printf("Valor inválido. ");
        }
    } while (valor2 == 0);

    printf("Resultado da divisão: %.2f\n", valor1 / valor2);

    return 0;
}

3.	Acrescentar uma mensagem de ’VALOR INVALIDO’ no exerc´ıcio ´ 1 caso o segundo valor informado seja ZERO.

#include <stdio.h>
#include <locale.h>

int main() {
    setlocale(LC_ALL, "Portuguese");

    float valor1, valor2;

    printf("Digite o primeiro valor: ");
    scanf("%f", &valor1);

    printf("Digite o segundo valor (diferente de zero): ");
    scanf("%f", &valor2);

    while (valor2 == 0) {
        printf("VALOR INVÁLIDO. Digite um valor diferente de zero: ");
        scanf("%f", &valor2);
    }

    printf("Resultado da divisão: %.2f\n", valor1 / valor2);

    return 0;
}

4.	Acrescentar uma mensagem de ’VALOR INVALIDO’ no exerc´ıcio ´ 2 caso o segundo valor informado seja ZERO.
#include <stdio.h>
#include <locale.h>

int main() {
    setlocale(LC_ALL, "Portuguese");

    float valor1, valor2;

    printf("Digite o primeiro valor: ");
    scanf("%f", &valor1);

    do {
        printf("Digite o segundo valor (diferente de zero): ");
        scanf("%f", &valor2);

        if (valor2 == 0) {
            printf("VALOR INVÁLIDO. ");
        }
    } while (valor2 == 0);

    printf("Resultado da divisão: %.2f\n", valor1 / valor2);

    return 0;
}

5.	Escreva um algoritmo para ler as notas da 1a. e 2a. avalia¸c˜oes de um aluno, calcule e imprima a m´edia (simples) desse aluno. S´o devem ser aceitos valores v´alidos durante a leitura (0 a 10) para cada nota.
#include <stdio.h>
#include <locale.h>

int main() {
    setlocale(LC_ALL, "Portuguese");

    float nota1, nota2, media;

    printf("Digite a nota da 1ª avaliação (0 a 10): ");
    scanf("%f", &nota1);
    while (nota1 < 0 || nota1 > 10) {
        printf("Valor inválido. Digite uma nota entre 0 e 10: ");
        scanf("%f", &nota1);
    }

    printf("Digite a nota da 2ª avaliação (0 a 10): ");
    scanf("%f", &nota2);
    while (nota2 < 0 || nota2 > 10) {
        printf("Valor inválido. Digite uma nota entre 0 e 10: ");
        scanf("%f", &nota2);
    }

    media = (nota1 + nota2) / 2;
    printf("Média: %.2f\n", media);

    return 0;
}
6.	Acrescente uma mensagem ’NOVO CALCULO (S/N)?’ ao final do exerc´ıcio ´ 5. Se for respondido ’S’ deve retornar e executar um novo c´alculo, caso contr´ario dever´a encerrar o algoritmo.

#include <stdio.h>
#include <locale.h>

int main() {
    setlocale(LC_ALL, "Portuguese");

    float nota1, nota2, media;
    char resposta;

    do {
        printf("Digite a nota da 1ª avaliação (0 a 10): ");
        scanf("%f", &nota1);
        while (nota1 < 0 || nota1 > 10) {
            printf("Valor inválido. Digite uma nota entre 0 e 10: ");
            scanf("%f", &nota1);
        }

        printf("Digite a nota da 2ª avaliação (0 a 10): ");
        scanf("%f", &nota2);
        while (nota2 < 0 || nota2 > 10) {
            printf("Valor inválido. Digite uma nota entre 0 e 10: ");
            scanf("%f", &nota2);
        }

        media = (nota1 + nota2) / 2;
        printf("Média: %.2f\n", media);

        printf("NOVO CÁLCULO (S/N)? ");
        scanf(" %c", &resposta);
    } while (resposta == 'S' || resposta == 's');

    return 0;
}

7.	Escreva um algoritmo para imprimir os n´umeros de 1 (inclusive) a 10 (inclusive) em ordem crescente.
#include <stdio.h>

int main() {
    for (int i = 1; i <= 10; i++) {
        printf("%d\n", i);
    }
    return 0;
}
8.	Escreva um algoritmo para imprimir os n´umeros de 1 (inclusive) a 10 (inclusive) em ordem decrescente.

#include <stdio.h>

int main() {
    for (int i = 10; i >= 1; i--) {
        printf("%d\n", i);
    }
    return 0;
}

9.	Escreva um algoritmo para imprimir os 10 primeiros n´umeros inteiros maiores que 100
#include <stdio.h>

int main() {
    for (int i = 101; i <= 110; i++) {
        printf("%d\n", i);
    }
    return 0;
}

10.	Ler um valor N e imprimir todos os valores inteiros entre 1 (inclusive) e N (inclusive). Considere que o N ser´a sempre maior que ZERO.

#include <stdio.h>
#include <locale.h>

int main() {
    setlocale(LC_ALL, "Portuguese");

    int N;

    printf("Digite um valor maior que zero: ");
    scanf("%d", &N);

    for (int i = 1; i <= N; i++) {
        printf("%d\n", i);
    }

    return 0;
}

11.	Modifique o exercício anterior para aceitar somente valores maiores que 0 para N. Caso o valor informado (para N) n˜ao seja maior que 0, dever´a ser lido um novo valor para N.

#include <stdio.h>
#include <locale.h>

int main() {
    setlocale(LC_ALL, "Portuguese");

    int N;

    do {
        printf("Digite um valor maior que zero: ");
        scanf("%d", &N);
    } while (N <= 0);

    for (int i = 1; i <= N; i++) {
        printf("%d\n", i);
    }

    return 0;
}

12.	Escreva um algoritmo que calcule e imprima a tabuada do 8 (1 a 10).
#include <stdio.h>

int main() {
    int i;

    for (i = 1; i <= 10; i++) {
        printf("8 x %d = %d\n", i, 8 * i);
    }

    return 0;
}
13.	Ler um valor inteiro (aceitar somente valores entre 1 e 10) e escrever a tabuada de 1 a 10 do valor lido
#include <stdio.h>
#include <locale.h>

int main() {
    setlocale(LC_ALL, "Portuguese");

    int valor;

    do {
        printf("Digite um valor entre 1 e 10: ");
        scanf("%d", &valor);
    } while (valor < 1 || valor > 10);

    for (int i = 1; i <= 10; i++) {
        printf("%d x %d = %d\n", valor, i, valor * i);
    }

    return 0;
}

14.	Fa¸ca um programa que leia um valor inteiro e crie um triˆangulo de *’s ao contr´ario. Por exemplo: Para n = 5: ***** **** *** ** *
#include <stdio.h>
#include <locale.h>

int main() {
    setlocale(LC_ALL, "Portuguese");

    int n;

    printf("Digite um valor: ");
    scanf("%d", &n);

    for (int i = n; i >= 1; i--) {
        for (int j = 1; j <= i; j++) {
            printf("*");
        }
        printf("\n");
    }

    return 0;
}

15.	Fa¸ca um algoritmo que calcule e escreva a m´edia aritm´etica dos n´umeros inteiros entre 15 (inclusive) e 100 (inclusive).

#include <stdio.h>
#include <locale.h>

int main() {
    setlocale(LC_ALL, "Portuguese");

    int soma = 0, contador = 0;

    for (int i = 15; i <= 100; i++) {
        soma += i;
        contador++;
    }

    float media = (float)soma / contador;
    printf("Média aritmética: %.2f\n", media);

    return 0;
}

16.	Uma loja est´a levantando o valor total de todas as mercadorias em estoque. Escreva um algoritmo que permita a entrada das seguintes informa¸c˜oes: a) o n´umero total de mercadorias no estoque; b) o valor de cada mercadoria. Ao final imprimir o valor total em estoque e a m´edia de valor das mercadorias.

#include <stdio.h>
#include <locale.h>

int main() {
    setlocale(LC_ALL, "Portuguese");

    int totalMercadorias;
    float valor, soma = 0;

    printf("Digite o número total de mercadorias: ");
    scanf("%d", &totalMercadorias);

    for (int i = 1; i <= totalMercadorias; i++) {
        printf("Digite o valor da mercadoria %d: ", i);
        scanf("%f", &valor);
        soma += valor;
    }

    float media = soma / totalMercadorias;

    printf("Valor total em estoque: %.2f\n", soma);
    printf("Média de valor das mercadorias: %.2f\n", media);

    return 0;
}
17.	O mesmo exerc´ıcio anterior, mas agora n˜ao ser´a informado o n´umero de mercadorias em estoque. Ent˜ao o funcionamento dever´a ser da seguinte forma: ler o valor da mercadoria e perguntar ‘MAIS MERCADORIAS (S/N)?’. Ao final, imprimir o valor total em estoque e a m´edia de valor das mercadorias em estoque.
#include <stdio.h>
#include <locale.h>

int main() {
    setlocale(LC_ALL, "Portuguese");

    float valor, soma = 0;
    int contador = 0;
    char resposta;

    do {
        printf("Digite o valor da mercadoria: ");
        scanf("%f", &valor);
        soma += valor;
        contador++;

        printf("MAIS MERCADORIAS (S/N)? ");
        scanf(" %c", &resposta);
    } while (resposta == 'S' || resposta == 's');

    float media = soma / contador;

    printf("Valor total em estoque: %.2f\n", soma);
    printf("Média de valor das mercadorias: %.2f\n", media);

    return 0;
}
