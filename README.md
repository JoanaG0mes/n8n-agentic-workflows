# ⚡ n8n Agentic Workflows: Guia de Automação & Agentes de IA

> Um guia prático e simplificado para entender, instalar e construir automações inteligentes e agentes de IA utilizando o **n8n**.

---

## 💡 O que é o n8n?

O **n8n** (pronuncia-se *nodemation*) é uma ferramenta de automação **low-code** e de código aberto. Ele funciona como uma "ponte universal" que conecta diferentes sistemas, aplicativos, bancos de dados e modelos de Inteligência Artificial sem a necessidade de escrever códigos complexos.

### 🧱 Os 3 Pilares da Automação Moderna

```text
               ┌─────────────────────────────────────────┐
               │    ORQUESTRADOR DE AUTOMAÇÃO (n8n)      │
               └────────────────────┬────────────────────┘
                                    │
         ┌──────────────────────────┼──────────────────────────┐
         ▼                          ▼                          ▼
  🧠 INTELIGÊNCIA ARTIFICIAL   ⚙️ CÓDIGO DETERMINÍSTICO     👤 SUPERVISÃO HUMANA
  Processa textos, toma        Executa regras fixas,       Garante segurança e
  decisões e entende           envia dados e roda de       aprova ações críticas
  contextos (LLMs).            forma rápida e previsível.  (Human-in-the-Loop).
```

---

## 🎯 Para quem é este repositório?

- 🛠️ **Desenvolvedores:** Querem integrar APIs, webhooks e scripts (Python/JavaScript) de forma visual e rápida.
- 📊 **Profissionais de Operações:** Querem automatizar tarefas repetitivas (como leitura de e-mails, atualização de CRMs e planilhas).
- 🛡️ **Equipes de TI e Segurança:** Precisam manter total controle e privacidade sobre os dados rodando o n8n em servidores próprios.

---

## 🤖 Como funcionam os Agentes de IA no n8n?

Em vez de uma automação engessada que só faz uma tarefa fixa, um **Agente de IA no n8n** possui:

1. **🧠 Cérebro (Modelo de IA):** Escolha qualquer IA como OpenAI (GPT-4o), Google Gemini, Claude 3.5 ou modelos locais (via Ollama).
2. **📋 Instruções (Prompt):** Regras claras de como a IA deve se comportar.
3. **💬 Memória (Contexto):** Lembra do histórico de conversas anteriores.
4. **🛠️ Ferramentas (Tools):** Conectores nativos do n8n (ex: enviar e-mail no Gmail, buscar em planilhas ou enviar mensagens no WhatsApp/Slack).

---

## ⚙️ Modos de Uso e Escala (Resumo Simples)

| Conceito | O que significa na prática? |
|:---|:---|
| **n8n Cloud** | Versão em nuvem pronta para uso imediato sem precisar instalar nada no seu computador. |
| **Self-Hosted (Local/Docker)** | Instalação gratuita em servidor próprio, garantindo total privacidade dos seus dados. |
| **Queue Mode (Modo Fila)** | Configuração avançada usando **Redis** para que milhares de automações rodem ao mesmo tempo sem travar o sistema. |
| **Model-Agnostic** | O n8n não prende você a uma única empresa de IA. Você pode trocar entre OpenAI, Gemini ou Claude quando quiser. |

---

## 🔒 Segurança e Boas Práticas

- 🔑 **Credenciais Criptografadas:** Senhas e chaves de API nunca ficam expostas no fluxo de trabalho.
- 🛡️ **Proteção contra Injeção de Prompt:** Higienização de textos recebidos de usuários antes de enviar para a IA.
- 👨‍💻 **Aprovação Humana:** Para ações sensíveis (como enviar um e-mail importante ou fazer pagamentos), a IA gera a resposta e aguarda sua aprovação antes de disparar.

---

## 🚀 Como Rodar Localmente (Via Docker)

Se você tem o Docker instalado na sua máquina, pode rodar o n8n em 1 minuto:

```bash
docker run -d --name n8n -p 5678:5678 -v n8n_data:/home/node/.n8n n8nio/n8n:latest
```

Após rodar o comando, abra o seu navegador e acesse: `http://localhost:5678`

---

## 📂 Estrutura das Pastas

```text
.
├── workflows/   # Fluxos de automação prontos para importar (arquivos .json)
├── docker/      # Arquivos de configuração de servidores (Docker Compose + Redis)
└── README.md    # Este guia prático e explicativo
```
