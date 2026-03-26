#include <stdio.h>
#include <stdlib.h>
#include <time.h>

int main() {
    int numero, palpite;

    srand(time(NULL));
    numero = rand() % 10 + 1;

    printf("Adivinhe o numero de 1 a 10\n");

    while (palpite != numero) {
        printf("Digite um numero: ");
        scanf("%d", &palpite);

        if (palpite == numero) {
            printf("Correto! Voce ganhou\n");
        } else if (palpite < numero) {
            printf("O numero e maior\n");
        } else {
            printf("O numero e menor\n");
        }
    }

    return 0;
}
