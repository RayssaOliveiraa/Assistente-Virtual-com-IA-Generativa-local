# 🎓 Guard Financeiro: Educador Financeiro com IA (Google Colab)

Este projeto apresenta o **Guard Financeiro**, um agente de inteligência artificial desenvolvido para ensinar conceitos de finanças pessoais de forma didática e personalizada. O sistema utiliza modelos de linguagem (LLMs) locais via **Ollama** e uma interface interativa em **Streamlit**.

Devido à demanda de hardware para processamento de IA, o projeto foi otimizado para rodar no **Google Colab**, aproveitando GPUs em nuvem e túneis de conexão segura.

---

## 🏗️ Arquitetura do Sistema

O projeto é dividido em camadas para garantir a execução em ambientes de nuvem temporários:

1. **Motor de IA (Ollama):** Servidor local que processa o modelo `Llama 3`.
2. **Interface (Streamlit):** Chat interativo para comunicação com o usuário.
3. **Túnel de Acesso (Ngrok):** Ponte de comunicação que expõe o servidor do Colab para a web.
4. **Contexto de Dados:** Leitura de arquivos JSON e CSV para personalização do atendimento.



---

## 🚀 Como Rodar o Projeto

Para executar o Guard Financeiro, acesse o notebook oficial e siga as etapas abaixo:

🔗 **[Link do Projeto no Google Colab](https://colab.research.google.com/drive/13jBd4OLbpMmgrAFASTzxwJSmIBkcQyqZ?usp=sharing)**

### Passo 1: Preparação e Instalação
Execute as células iniciais para instalar o `Ollama`, `Streamlit` e a dependência de descompressão `zstd`.

### Passo 2: Inicialização da IA
O servidor Ollama é iniciado em segundo plano e o modelo `Llama 3` é baixado automaticamente. 
> *Nota: Este processo pode levar alguns minutos dependendo da conexão do Google.*

### Passo 3: Configuração do Ngrok
Para visualizar a interface, é necessário um token gratuito do [Ngrok](https://ngrok.com/):
1. Crie sua conta e copie o `Authtoken`.
2. Insira o token na célula de execução do túnel.
3. Clique no link gerado para abrir o chat.

---

## 📂 Estrutura de Dados (Pasta `/data`)

O agente utiliza arquivos locais para fundamentar suas explicações. **Atenção:** Como o Colab é efêmero, esses arquivos devem ser carregados no menu lateral a cada nova sessão:

* `perfil_investidor.json`: Dados e objetivos do cliente.
* `transacoes.csv`: Histórico financeiro para exemplos práticos.
* `produtos_financeiros.json`: Catálogo educativo de ativos.
* `historico_atendimento`: Catálogo educativo de ativos.

---

## ⚖️ Diretrizes do Agente (System Prompt)

O **Guard Financeiro** segue regras estritas para garantir uma educação segura:
- **Proibição de Recomendações:** O agente explica como os investimentos funcionam, mas nunca indica compra ou venda de ativos específicos.
- **Linguagem Acessível:** Respostas curtas (até 3 parágrafos), jovens e sem "economês" excessivo.
- **Foco Temático:** O agente recusa perguntas que não sejam sobre finanças pessoais.

---

## 🛠️ Tecnologias Utilizadas

- **Python 3.10+**
- **Streamlit** (Interface)
- **Ollama / Llama 3** (Inteligência Artificial)
- **Ngrok** (Tunelamento de Rede)
- **Pandas** (Tratamento de Dados)

---
*Este projeto foi desenvolvido para fins educacionais e de demonstração tecnológica.*
