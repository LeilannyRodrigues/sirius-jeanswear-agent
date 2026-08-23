# 🤖 Assistente Virtual RAG - Sirius Jeanswear

Assistente inteligente integrado ao Telegram capaz de responder a dúvidas operacionais e políticas internas da empresa **Sirius Jeanswear** utilizando arquitetura RAG (Retrieval-Augmented Generation).

---

## 📌 Visão Geral do Projeto
O objetivo deste projeto é otimizar o atendimento interno e a consulta de informações para colaboradores, permitindo o acesso rápido a documentos operacionais via Telegram através de um agente automatizado e contextualizado.

---

## 🛠️ Arquitetura e Tecnologias
- **Orquestração de Fluxo:** [n8n](https://n8n.io/)
- **Modelo de Linguagem (LLM):** Google Gemini 1.5 Flash
- **Embeddings & Base Vetorial:** Cohere Embeddings + Vector Store (n8n In-Memory / Qdrant)
- **Canal de Comunicação:** Telegram Bot API
- **Documento Base:** Manual de Operações Internas - Sirius Jeanswear (PDF)

---

## 🚀 Como Executar o Projeto

### Pré-requisitos
1. Instância do **n8n** (rodando localmente via Docker/npx ou hospedado na nuvem).
2. Conta no Telegram e um bot criado via `@BotFather` para obter o `HTTP API Token`.
3. Chaves de API configuradas para:
   - Google Gemini API
   - Cohere API

### Passo a Passo
1. Importe o arquivo JSON do fluxo (`workflow.json`) localizado neste repositório para o seu n8n.
2. Configure as credenciais das APIs no n8n (Telegram, Gemini, Cohere).
3. Faça o upload do documento PDF na base de conhecimento.
4. Ative a chave **Publish / Active** no n8n.
5. Inicie a conversa com o bot no Telegram.

---

## 💬 Exemplos de Perguntas e Respostas

> **Usuário:** Qual é a política de trocas da Sirius Jeanswear?  
> **Bot:** *Com base no Manual de Operações Internas, as trocas podem ser realizadas em até 30 dias mediante apresentação do comprovante de compra e etiqueta afixada.*  
> 📄 *Fonte: Manual_Operacoes_Sirius.pdf*

> **Usuário:** Quem é o responsável pelo setor de logística?  
> **Bot:** *O setor de logística é gerenciado por [Nome do Responsável], conforme a Seção 3 do Manual Interno.*  
> 📄 *Fonte: Manual_Operacoes_Sirius.pdf*

---

## 📸 Demonstração do Funcionamento

*(Adicione aqui os prints do bot respondendo no Telegram e do fluxo no n8n)*

![Fluxo n8n](./prints/n8n-workflow.png)
![Demonstração Telegram](./prints/telegram-demo.png)
