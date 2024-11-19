- 👋 Hi, I’m @JoiceVilela
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...

import random

def jogo_adivinhacao():
    print("Bem-vindo ao jogo de adivinhação!")
    numero_secreto = random.randint(1, 100)
    tentativas = 0

    while True:
        try:
            palpite = int(input("Digite um número entre 1 e 100: "))
            tentativas += 1

            if palpite < numero_secreto:
                print("Muito baixo! Tente novamente.")
            elif palpite > numero_secreto:
                print("Muito alto! Tente novamente.")
            else:
                print(f"Parabéns! Você acertou o número secreto {numero_secreto} em {tentativas} tentativas.")
                break
        except ValueError:
            print("Por favor, digite um número válido.")

# Inicia o jogo
jogo_adivinhacao()
