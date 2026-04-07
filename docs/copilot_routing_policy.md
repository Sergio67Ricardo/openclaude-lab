# Política de Roteamento de Modelos

## Escopo

Este documento define a política de roteamento de modelos para OpenClaude dentro deste repositório.

## Governança de modelos

- Padrão: `OpenClaude + Ollama local`
- Executor principal: `Cursor Pro`
- Fallback controlado: `MiniMax`

## Regras de roteamento

1. Usar Ollama local sempre que disponível.
2. Manter Cursor Pro como executor preferencial para tarefas de código e edições.
3. Acionar MiniMax apenas quando a camada padrão estiver indisponível ou instável.
4. Para integrações externas, como Roteirista IA, aplicar o roteamento descrito neste documento.

## Exemplo de configuração

- `default`: Ollama local
- `fallback`: MiniMax
- `executor`: Cursor Pro

## Observações

- A política deve ser revisada sempre que houver mudança no conjunto de backends suportados.
- Documentar qualquer exceção ou ajuste de roteamento no próprio repositório.
