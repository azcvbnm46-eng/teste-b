import random

while True:
    numero = random.randint(1, 10)
    tentativas = 0

    print("\n🎮 Adivinhe o número de 1 a 10")

    while True:
        palpite = int(input("Digite o número: "))
        tentativas += 1

        if palpite == numero:
            print(f"🎉 Correto! Você ganhou em {tentativas} tentativas")
            break
        elif palpite < numero:
            print("🔼 O número é maior")
        else:
            print("🔽 O número é menor")

    jogar_novamente = input("Quer jogar novamente? (s/n): ").lower()
    
    if jogar_novamente != 's':
        print("👋 Até logo!")
        break
