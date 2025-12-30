# Arquitetura do Chatbot GJ

Este projeto segue o princípio de **menos nós, mais clareza**.

## Decisões arquiteturais

- IA recebe a mensagem quase crua
- A lógica pesada fica no prompt, não no workflow
- Switch por intenção substitui múltiplos IFs
- Um único nó de envio de mensagens

## Benefícios

- Menor custo operacional
- Debug mais simples
- Alta reutilização
