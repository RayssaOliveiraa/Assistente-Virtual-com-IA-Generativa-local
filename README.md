# 🎓 Guard Financeiro: Educador Financeiro com IA (Google Colab)

Este projeto apresenta o **Guard Financeiro**, um agente de inteligência artificial desenvolvido para ensinar conceitos de finanças pessoais de forma didática e personalizada. O sistema utiliza modelos de linguagem (LLMs) locais via **Ollama** e uma interface interativa em **Streamlit**.

Devido à alta demanda de hardware para processamento de IA, o projeto foi otimizado para rodar na infraestrutura de nuvem do **Google Colab**, garantindo acesso gratuito a GPUs e contornando limitações de memória local.

---

## 🏗️ Arquitetura do Sistema

O projeto integra diferentes tecnologias para permitir a execução em nuvem:

1. **Motor de IA (Ollama):** Servidor local no Colab que processa o modelo `Llama 3`.
2. **Interface (Streamlit):** Chat interativo para comunicação em tempo real.
3. **Túnel de Acesso (Ngrok):** Ponte de rede que expõe o servidor do Colab para o seu navegador.
4. **Contexto de Dados:** Base de conhecimento extraída de arquivos JSON e CSV.



---

## 📂 Estrutura de Dados e Persistência

**Atenção:** O Google Colab possui um armazenamento **efêmero**. Isso significa que toda vez que a página é reiniciada ou a sessão encerrada, os arquivos são apagados. 

Para que o agente funcione, o usuário deve **obrigatoriamente**:
1. Criar a pasta `./data/` no menu lateral de arquivos do Colab.
2. Criar a pasta `./src/` (opcional para organização de scripts).
3. Fazer o **upload manual** dos seguintes arquivos para dentro da pasta `/data`:

* `perfil_investidor.json`: Dados demográficos e objetivos do cliente.
* `transacoes.csv`: Histórico financeiro para análise de gastos.
* `historico_atendimento.csv`: Registro de interações passadas para manter a continuidade.
* `produtos_financeiros.json`: Catálogo educativo de ativos disponíveis.

---

## 🚀 Como Rodar o Projeto

🔗 **[Link do Projeto no Google Colab](https://colab.research.google.com/drive/13jBd4OLbpMmgrAFASTzxwJSmIBkcQyqZ?usp=sharing)**

1. **Instalação:** Execute as células iniciais para preparar o ambiente (Streamlit, Ngrok e dependências de sistema).
2. **Servidor de IA:** Inicie o Ollama e aguarde o download do modelo `Llama 3`.
3. **Arquivos:** Após criar a pasta `/data`, anexe seus arquivos JSON e CSV.
4. **Túnel Ngrok:** - Insira seu `Authtoken` (obtido gratuitamente em ngrok.com).
   - Execute a célula final e clique no link gerado para abrir o chat.

---

## ⚖️ Diretrizes do Agente (System Prompt)

O **Guard Financeiro** segue regras rígidas para garantir uma educação financeira ética:
- **Sem Recomendações:** O agente explica conceitos, mas nunca indica a compra ou venda de ativos específicos.
- **Linguagem Jovem:** Respostas curtas (até 3 parágrafos) e sem "economês" complexo.
- **Foco Temático:** O agente recusa educadamente qualquer pergunta fora do tema de finanças.

---

## 🛠️ Tecnologias Utilizadas

- **Python 3.10+**
- **Streamlit** (Interface Visual)
- **Ollama / Llama 3** (Inteligência Artificial Local)
- **Ngrok** (Tunelamento de Rede)
- **Pandas** (Análise de Dados)

---
*Este projeto foi desenvolvido para fins educacionais e de demonstração tecnológica.*
