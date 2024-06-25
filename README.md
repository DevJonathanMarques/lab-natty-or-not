# PROJETO IA DIO - NATTY OR NOT?

## 📒 Descrição
O projeto consiste em criar um conteúdo utilizando inteligência artificial, portanto, eu criei com o ChatGPT um ChatBot, onde você pode ter um diálogo simples com ele.

## 🤖 Tecnologias Utilizadas
ChatGPT

## 🧐 Processo de Criação
Pensei em utilizar a inteligência artificial para criar algo relacionado a inteligência artificial, até que veio a ideia do ChatBot. No ChaGPT, pedi que ele criasse um ChatBot simples para mim. A primeira versão não ficou muito boa, pois a mensagem que o usuário digitou não faria diferença, já que a resposta seria aleatória. Então, eu pedi que ele criasse um ChatBot em que fosse possível ter um diálogo simples.

## 🚀 Resultados
O código abaixo foi o resultado dos meus prompts do ChatGPT, caso você queria testar, é só rodá-lo no terminal e dialogar com as mensagens: **Oi**, **Como você está?**, **Qual é o seu nome?**, **Adeus**, **Sair**.

```python
import random

# Dicionário de padrões e respostas
padroes_respostas = {
    "oi": ["Olá!", "Oi!", "E aí!"],
    "como você está?": ["Estou bem, obrigado por perguntar!", "Estou ótimo! E você?", "Estou bem, e você?"],
    "qual é o seu nome?": ["Meu nome é ChatBot.", "Você pode me chamar de ChatBot.", "Sou o ChatBot!"],
    "adeus": ["Até mais!", "Tchau!", "Até a próxima!"],
    "sair": ["Até mais!", "Tchau!", "Foi bom conversar com você!"],
}

# Função para responder às perguntas do usuário
def responder(pergunta):
    for padrao, respostas in padroes_respostas.items():
        if padrao in pergunta:
            return random.choice(respostas)
    return "Desculpe, não entendi o que você disse."

# Função principal que lê as perguntas do usuário e responde
def main():
    print("Bem-vindo ao ChatBot! (Digite 'sair' para sair)")
    while True:
        pergunta = input("Você: ").strip().lower()
        if pergunta == "sair":
            print("Até mais!")
            break
        resposta = responder(pergunta)
        print("ChatBot:", resposta)

# Executar o chatbot
if __name__ == "__main__":
    main()
```
