# Vitality Fitness AI Chatbot

Este repositório contém uma implementação de um assistente virtual inteligente para a academia **Vitality Fitness Center**. O chatbot utiliza a API da OpenAI (modelo `gpt-4o-mini`) para fornecer informações sobre modalidades, horários, localização e motivar os alunos.

## Funcionalidades

* **Streaming de Respostas:** Respostas geradas em tempo real para uma experiência mais fluida.
* **Gestão de Memória:** Mantém um histórico das últimas 5 interações para contexto (janela deslizante).
* **Persona Customizada:** Configurado com um *System Prompt* robusto que define a identidade visual, valores e tom de voz da academia.
* **Integração com Colab:** Utiliza o `userdata` do Google Colab para gerenciamento seguro de chaves de API.

## Tecnologias Utilizadas

* **Linguagem:** Python
* **IA:** OpenAI API (`gpt-4o-mini`)
* **Ambiente:** Google Colab / Jupyter Notebook
* **Bibliotecas:** `openai`, `os`

## Pré-requisitos

Antes de rodar o projeto, você precisará de:

1.  Uma chave de API da [OpenAI](https://platform.openai.com/).
2.  Uma conta no Google para acessar o Colab.

## Configuração

1.  Abra o arquivo `.ipynb` no Google Colab.
2.  No menu lateral esquerdo, clique no ícone de chave (**Secrets**).
3.  Adicione uma nova chave com o nome `OPENAI_API_KEY` e cole o seu token no valor.
4.  Ative a opção "Notebook access" para essa chave.

## Como Usar

Execute as células do notebook. O chat será iniciado no próprio console. 

**Comandos especiais:**
* Para encerrar a conversa, digite: `sair`, `fim` ou `tchau`.

---

## Estrutura do Código

* **`system_prompt`**: Contém todo o conhecimento base sobre a Vitality Fitness (endereço, aulas, contatos).
* **`academia_chat()`**: Função principal que gerencia o envio de mensagens e a atualização do histórico.
* **`historico.pop(1)`**: Lógica para manter o contexto sem exceder o limite de tokens do modelo.

## Licença

Este projeto é para fins de estudo e demonstração técnica.
