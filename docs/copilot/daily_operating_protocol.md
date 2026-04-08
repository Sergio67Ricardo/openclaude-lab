
# Daily Operating Protocol
**Versão:** 1.0  
**Status:** Ativo  
**Escopo:** uso diário do ambiente OpenClaude no VS Code  
**Objetivo:** padronizar abertura, validação, decisão de camada, execução e fechamento da sessão

---

## 1. Finalidade

Este protocolo existe para reduzir improviso, evitar uso inconsistente das camadas e transformar o ambiente em rotina repetível.

Ele deve ser:

- curto
- operacional
- manual
- fácil de aplicar em 1 a 2 minutos
- compatível com o fluxo real no VS Code

---

## 2. Sequência padrão da sessão

```text
abrir workspace → validar runtime → escolher camada → iniciar sessão com objetivo claro → trabalhar → registrar estado de saída
```

---

## 3. Pré-início da sessão

Antes de começar, verificar:

- workspace correto aberto no VS Code
- branch correta
- repositório limpo ou com estado conhecido
- Ollama ativo, quando a camada local for a escolhida
- modelo local disponível
- objetivo da sessão claro

### Checklist
- [ ] workspace correto
- [ ] branch correta
- [ ] `git status` conhecido
- [ ] runtime necessário ativo
- [ ] tarefa atual definida

---

## 4. Validação do runtime

## 4.1 Quando a sessão for local
Validar:

- Ollama ativo
- endpoint funcional
- modelo local disponível
- OpenClaude abre sem erro

### Referência operacional
- servidor Ollama ativo
- OpenClaude iniciado no VS Code
- resposta local funcional antes de começar tarefa relevante

---

## 4.2 Quando a sessão exigir cloud
Validar:

- necessidade real de cloud
- ausência de conteúdo sensível
- justificativa de escalonamento
- crédito/saldo disponível, se aplicável

---

## 5. Escolha da camada

## 5.1 Usar VS Code + Ollama + OpenClaude
Quando a tarefa for de:

- análise
- preparação
- revisão
- documentação
- snippets
- regex
- exploração técnica
- teste de hipótese

---

## 5.2 Usar VS Code + MiniMax + OpenClaude
Somente quando:

- houve tentativa local suficiente
- a resposta local teve baixa utilidade prática
- a tarefa exige mais precisão analítica
- o contexto ficou pesado demais para o local

---

## 5.3 Usar Cursor Pro
Quando houver:

- alteração real no codebase
- refatoração multi-arquivo
- debugging estrutural
- integração entre módulos
- consolidação final de implementação

### Regra curta
```text
Pensar localmente.
Escalar para cloud com critério.
Executar no Cursor quando houver mudança real.
```

---

## 6. Início da sessão

Antes de trabalhar, registrar mentalmente ou em texto curto:

- tarefa atual
- objetivo imediato
- camada escolhida
- critério de sucesso

### Template mínimo
```text
Tarefa:
Objetivo imediato:
Camada escolhida:
Critério de sucesso:
```

---

## 7. Regras durante o trabalho

- não mudar de camada sem motivo explícito
- não escalar para cloud por preferência
- não enviar segredos ou contexto sensível
- não usar Cursor para brainstorming pequeno
- não usar OpenClaude local como executor principal de mudanças críticas
- manter escopo da sessão pequeno e claro

---

## 8. Encerramento da sessão

Ao finalizar, registrar:

- o que foi feito
- o que ficou pendente
- próxima ação recomendada
- se houve nova decisão relevante de governança

### Template mínimo
```text
Feito:
Pendente:
Próximo passo:
Decisão relevante:
```

### Checklist
- [ ] resultado da sessão conhecido
- [ ] pendência identificada
- [ ] próximo passo definido
- [ ] decisão relevante registrada, se houver

---

## 9. Exceções permitidas

É aceitável quebrar o fluxo padrão quando houver:

- indisponibilidade do runtime local
- urgência operacional real
- falha local já confirmada
- necessidade pontual de qualidade superior

Toda exceção deve ser:

- consciente
- pontual
- justificável

---

## 10. O que não fazer agora

- não automatizar o roteamento de modelos
- não introduzir multiagente
- não criar MCP desnecessário
- não transformar este protocolo em processo pesado
- não depender de memória informal em vez de aplicar o protocolo

---

## 11. Dependências e pré-condições

Este protocolo pressupõe que:

- a FASE 0 foi concluída
- o OpenClaude foi validado para uso diário local
- o checklist de confiança e segurança está versionado
- o log de validação existe e pode ser atualizado
- o VS Code é o ambiente principal de operação
- o Cursor Pro continua como executor principal de código

---

## 12. Artefatos relacionados

Este protocolo deve ser lido em conjunto com:

- `docs/copilot/openclaude_trust_and_security_checklist.md`
- `docs/copilot/validations/openclaude_validation_log.md`
- `docs/copilot/Manual_Profissional_Copilot_Tecnico_Estruturado.md`
- `docs/copilot/Integracao_OpenClaude_Roteirista_IA.md`
- `docs/copilot_routing_policy.md`

---

## 13. Política de revisão

Este protocolo deve ser revisto quando houver:

- mudança relevante no fluxo de uso
- alteração da política de roteamento
- troca de modelo local
- mudança de estratégia cloud/local
- evidência de fricção recorrente no uso diário

Recomendação mínima:
- revisar após 3 a 5 sessões reais de uso
- depois consolidar ajustes antes de automatizar qualquer parte

---

## 14. Regra final

```text
Abrir com estado conhecido.
Validar antes de começar.
Escolher camada com critério.
Fechar com saída registrada.
```
