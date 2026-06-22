# 🐢 TurtleRH - Assistente Virtual de Recursos Humanos

### Sistema de automação com IA, integração com banco de dados e fluxo inteligente de atendimento via Telegram

[![Status do Projeto](https://img.shields.io/badge/Status-Concluído-success.svg)]()
[![Tecnologias](https://img.shields.io/badge/n8n%20%7C%20MySQL%20%7C%20IA-Automação-blue.svg)]()
[![Tipo](https://img.shields.io/badge/Projeto-IA%20Aplicada-orange.svg)]()

---

### 📌 Sobre o Projeto

O **TurtleRH** é um sistema de assistente virtual de Recursos Humanos desenvolvido com foco em automação de processos e aplicação prática de Inteligência Artificial.

O projeto simula um ambiente real de atendimento de RH, onde funcionários interagem via Telegram e recebem respostas automatizadas baseadas em regras de negócio, consulta a banco de dados e uma base de conhecimento estruturada.

A solução integra diferentes tecnologias para demonstrar como IA pode ser aplicada em fluxos reais de empresas, reduzindo trabalho manual e automatizando respostas.

---

### ⚙️ Funcionalidades

- Atendimento automatizado via Telegram  
- Identificação de funcionários por nome completo  
- Consulta de dados em banco MySQL (Railway)  
- Retorno de informações como férias e banco de horas  
- Respostas baseadas em políticas internas de RH  
- Uso de IA para interpretação de mensagens  
- Separação entre dados estruturados e base de conhecimento  

---

### 🧠 Arquitetura do Sistema

O sistema é dividido em três componentes principais:

## Agente de IA (TurtleRH)
Responsável por interpretar as mensagens, aplicar regras do prompt e decidir quando consultar o banco de dados ou a base de conhecimento.

## Automação (n8n)
Orquestra todo o fluxo do sistema:

- Recebe mensagens do Telegram  
- Encaminha para o agente de IA  
- Executa consultas no MySQL quando necessário  
- Retorna a resposta ao usuário  

## Banco de Dados (MySQL - Railway)
Armazena informações dos funcionários, como:

- Nome completo  
- Saldo de férias  
- Banco de horas  

O banco pode ser recriado utilizando o arquivo `database.sql`.

---

### 📂 Estrutura do Projeto

```plaintext
Turtle-RH/
│
├── Database/
│   └── database.sql
│
├── Workflow/
│   ├── workflow-telegram.json
│   └── workflow-politicas.json
│
├── Prompt/
│   └── prompt-agente.txt
│
│
└── README.md
```

## 🔁 Fluxo do Sistema

1. Usuário envia mensagem no Telegram  
2. n8n recebe e inicia o workflow  
3. O agente TurtleRH interpreta a mensagem  
4. Consulta MySQL quando necessário  
5. Aplica regras do prompt de IA  
6. Retorna resposta ao usuário  

---

### 🧠 Regras do Agente
- Responder apenas dúvidas relacionadas a RH
- Solicitar nome completo do funcionário caso não informado
- Não inventar dados pessoais
- Usar banco de dados para informações individuais
- Usar base de conhecimento para políticas gerais

---

### 🛠️ Tecnologias Utilizadas

| Categoria               | Tecnologias               |
| :---------------------- | :---------------------    |
| Automação               | n8n                       |
| Banco de Dados          | MySQL (Railway)           |
| Comunicação             | Telegram Bot API          |
| Inteligência Artificial | Cohere, RAG, Agentes de IA|
| Versionamento           | Git & GitHub              |

---

### 📸 Demonstração
Fluxo no n8n

<img width="806" height="414" alt="Workflow" src="https://github.com/user-attachments/assets/422c3556-9b28-4096-a1ed-28736091e669" />

Conversa no Telegram

<img width="720" height="494" alt="ChatBot" src="https://github.com/user-attachments/assets/ed4f049c-8cc5-4d33-9e41-727dc881a8a4" />

Banco de Dados

<img width="795" height="332" alt="Tabela Funcionários" src="https://github.com/user-attachments/assets/f2fda4f1-1c97-45f1-afa3-df7cc07d53b1" />

---

### 📚 Contexto do Projeto

Este projeto foi desenvolvido durante uma imersão prática da Alura + Oracle Next Education (ONE), com foco em:

- Inteligência Artificial aplicada
- Automação de processos reais
- Integração entre sistemas
- Construção de agentes inteligentes
