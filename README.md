#include <stdio.h>
#include <stdlib.h>
#include <time.h>

int main() {
    int numero, palpite, tentativas = 0;
    char jogar_novamente;

    srand(time(0));

    do {
        numero = rand() % 10 + 1;
        tentativas = 0;

        printf("\n🎮 Adivinhe o número de 1 a 10\n");

        do {
            printf("Digite o número: ");
            scanf("%d", &palpite);
            tentativas++;

            if (palpite == numero) {
                printf("🎉 Correto! Você ganhou em %d tentativas\n", tentativas);
            } else if (palpite < numero) {
                printf("🔼 O número é maior\n");
            } else {
                printf("🔽 O número é menor\n");
            }

        } while (palpite != numero);

        printf("Quer jogar novamente? (s/n): ");
        scanf(" %c", &jogar_novamente);

    } while (jogar_novamente == 's' || jogar_novamente == 'S');

    printf("👋 Até logo!\n");

    return 0;
}
