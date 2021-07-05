# Jogo-de-Adivinhacao
Jogo de adivinhacao desenvolvido na linguagem Python
print("_________________________________")
print("Bem vindo ao jogo de Adivinhação!")
print("_________________________________")

numero_secreto = 42
total_de_tentativas = 3
rodada = 1


while(rodada <= total_de_tentativas):
    print("Tentativa {} de {}".format(rodada, total_de_tentativas))
    chute_str = input("digite seu numero: ")
    chute = int(chute_str)
    print("voce digitou", chute_str)

    acertou = numero_secreto == chute
    maior   = chute > numero_secreto
    menor   = chute < numero_secreto


    if (acertou):
       print("voce acertou")
    else:
        if (maior):
            print ("voce errou, seu chute foi maior que o numero secreto.")
        elif (menor):
            print("voce errou, seu chute foi menor que o numero secreto.")

            rodada = rodada + 1

    print("Fim do Jogo")
