# Sirius AI Assistant - Bot de Atendimento e RH

Assistente virtual desenvolvido para automação de atendimento via Telegram, utilizando RAG (Retrieval-Augmented Generation) para responder dúvidas sobre regras, políticas de RH e conduta com precisão.

## 🛠️ Tecnologias Utilizadas
- **n8n**: Orquestração do fluxo de automação
- **Google Gemini API**: Modelo de linguagem (LLM)
- **Vector Store (In-Memory)**: Armazenamento vetorial para busca semântica (RAG)
- **Cohere Embeddings**: Geração de vetores para os documentos
- **Telegram Bot API**: Interface de comunicação com os usuários

## 🧱 Arquitetura do Fluxo
1. **Trigger**: O nó do Telegram captura as mensagens recebidas no chat.
2. **Contexto & RAG**: A mensagem do usuário busca trechos relevantes armazenados no Vector Store através de busca vetorial.
3. **Processamento**: O AI Agent envia o prompt enriquecido com o contexto resgatado para a API do Google Gemini.
4. **Resposta**: O bot responde diretamente ao usuário no Telegram.

## ❓ Exemplo de perguntas e Respostas Suportadas pelo Agente
O agente foi treinado com a base de conhecimento interna para responder a tópicos como:
- **Políticas de RH:** Solicitação de informações sobre folha de pagamento, benefícios e reembolsos de despesas (como retenção fiscal e vouchers de reembolso).
- **Regras e Conduta:** Diretrizes de integridade, conduta ética, uso adequado dos canais da empresa e ambiente de trabalho.
- **Procedimentos Internos:** Orientações sobre o uso do Manual de Operações e prazos para envio de documentações financeiras/contábeis.

## 🚀 Como Importar e Rodar este Projeto
1. Instale/Suba uma instância do n8n (local ou via Railway).
2. Crie um novo Workflow e clique em **`...` > Import from File**.
3. Selecione o arquivo `.json` deste repositório.
4. Configure as credenciais no n8n para:
   - Telegram Bot API Token
   - Google Gemini API Key
   - Cohere API Key
5. Ative o Workflow em **Published**.

## 🔗 Links Úteis
- **Bot no Telegram**: [@siriusjeansaiBot](https://t.me/siriusjeansaiBot)
- **Vídeo de Demonstração**: 


https://github.com/user-attachments/assets/c4c9dbf0-a12b-4d45-9d33-f5ddc8baef82









