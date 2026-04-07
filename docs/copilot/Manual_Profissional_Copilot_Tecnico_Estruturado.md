# Manual Profissional Copilot Técnico Estruturado

## Objetivo

Este manual descreve a operação estruturada do Copilot técnico no contexto do projeto OpenClaude.

## Governança de modelos

- `OpenClaude + Ollama local` é a camada padrão para execução de agentes.
- `MiniMax` atua como fallback controlado, disponível quando a pilha padrão não estiver disponível.
- `Cursor Pro` permanece como executor principal para workflows de código e edição.

## Uso operacional

1. Iniciar OpenClaude no ambiente local.
2. Garantir que o servidor Ollama esteja ativo para inferência local.
3. Selecionar o provedor local em `/provider` ou via variáveis de ambiente.
4. Usar o Copilot com foco em fluxo de trabalho de desenvolvimento e suporte técnico.

## Papéis e responsabilidades

- Operador técnico: validar disponibilidade da camada padrão e monitorar o fallback MiniMax.
- Integrador: documentar e manter políticas de roteamento e instruções no repositório.
- Executor principal: confiar em Cursor Pro sempre que houver suporte adequado para a tarefa.

## Práticas recomendadas

- Usar a documentação do projeto para decidir quando ativar o fallback MiniMax.
- Preferir modelos locais no conjunto padrão para reduzir latência e dependência externa.
- Manter registros curtos de configurações aplicadas em cada sessão.
