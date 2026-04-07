# Integração OpenClaude com Roteirista IA

## Objetivo

Documentar a integração entre OpenClaude e o projeto Roteirista IA, preservando a governança de modelos do repositório.

## Contexto de integração

- OpenClaude opera como camada de orquestração.
- Ollama local é o backend padrão para inferência.
- MiniMax é fallback controlado.
- Cursor Pro permanece como executor principal nas tarefas de roteiro e edição.

## Fluxo de trabalho

1. O Roteirista IA envia solicitações para o OpenClaude.
2. OpenClaude roteia a tarefa ao modelo local Ollama sempre que possível.
3. Em caso de indisponibilidade, o fallback MiniMax é acionado sob controle humano.
4. Cursor Pro executa ações de código e direção de fluxo.

## Configuração

- Garantir que o servidor Ollama esteja disponível para tarefas de roteiro.
- Definir as rotas de modelo com base na política de roteamento documentada.
- Verificar compatibilidade de prompt e função entre OpenClaude e Roteirista IA.

## Observações

- A integração deve ser simples e leve, sem alterar o código-fonte do OpenClaude.
- Documentar alterações de configuração no repositório para rastreabilidade.
