print("_________________________________")
print("Bem vindo ao jogo de Adivinhação!")
print("_________________________________")

numero_secreto = 42
total_de_tentativas = 3
rodada = 1


for rodada in range (1, total_de_tentativas + 1):
    print("Tentativa {} de {}".format(rodada, total_de_tentativas))
    chute_str = input("digite um numero entre 1 e 100: ")
    chute = int(chute_str)
    print("voce digitou", chute_str)

    if(  chute < 1 or chute > 100 ):
        print ("voce deve digitar um numero entre 1 e 100!!!")
        continue #volta para o inicio do programa

    acertou = numero_secreto == chute
    maior   = chute > numero_secreto
    menor   = chute < numero_secreto


    if (acertou):
       print("voce acertou")
       break #Para o programa
    else:
        if (maior):
            print ("voce errou, seu chute foi maior que o numero secreto.")
        elif (menor):
            print("voce errou, seu chute foi menor que o numero secreto.")

            rodada = rodada + 1

    print("Fim do Jogo")
