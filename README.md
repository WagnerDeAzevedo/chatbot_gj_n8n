# 🤖 Chatbot WhatsApp com IA — n8n + OpenAI

Este projeto demonstra uma arquitetura **enxuta e funcional** de chatbot para WhatsApp,
utilizando **n8n** como orquestrador e **OpenAI** como agente de IA.

O foco é **automação prática**, clareza arquitetural e fácil reaproveitamento
para outros projetos de atendimento, agendamento e suporte.

---

## 🎯 Objetivo

- Receber mensagens do WhatsApp
- Interpretar intenção do usuário via IA
- Responder automaticamente ou direcionar fluxo
- Manter o **mínimo de nós possível**
- Ser reutilizável como base para novos bots

---

## 🧱 Arquitetura (resumida)

Fluxo principal (`chatbot_gj`):

1. Entrada via webhook (WhatsApp)
2. Padronização de dados do usuário
3. Agente de IA com saída estruturada (JSON)
4. Switch por intenção
5. Envio de resposta ao WhatsApp

Arquitetura propositalmente simples para:
- reduzir custo
- facilitar manutenção
- acelerar novos projetos

---

## ♻️ Como reutilizar este projeto

Este repositório foi pensado como **core reutilizável**.

O workflow principal **não depende da origem da mensagem**.
Ele assume que a entrada já foi padronizada por um adapter externo
(ex: WhatsApp, API REST, formulário, CRM).

### Entrada esperada
- `mensagem_usuario`
- `telefone_usuario`

Qualquer canal que entregue esses campos pode reutilizar
o mesmo fluxo sem alterações estruturais.

### Benefícios
- Reuso imediato para novos clientes
- Troca de canal sem reescrever lógica
- Menor custo de manutenção

---

## 🧠 Intenções suportadas

- `saudacao`
- `preco_servicos`
- `agendamento`
- `humano`

Novas intenções podem ser adicionadas sem inflar o workflow.

---

## 🔐 Segurança & LGPD

- Nenhuma credencial no repositório
- Tokens via variáveis de ambiente
- Nenhum dado sensível persistido
- Projeto preparado para integrações futuras (ex: sistemas de agenda)

---

## 🧭 Evolução planejada

- Integração com sistemas de agendamento
- Inclusão de novas intenções sem inflar o workflow
- Monitoramento e métricas de atendimento
- Reuso da arquitetura para múltiplos clientes

---

## 📄 Licença

Uso educacional e demonstrativo.
