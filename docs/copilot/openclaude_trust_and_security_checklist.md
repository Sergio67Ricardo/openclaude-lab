
# 🔒 OpenClaude — Checklist de Confiança e Segurança (v1)

> Objetivo: validar que o OpenClaude instalado é seguro o suficiente para uso local contínuo no ambiente de desenvolvimento.

---

## 1. Origem e Proveniência

```text
[ ] Origem do OpenClaude identificada (repositório, fork ou distribuição)
[ ] Método de instalação conhecido (npm, clone + build, binário, etc.)
[ ] Fonte rastreável e reproduzível
[ ] NÃO instalado a partir de link indireto ou fonte desconhecida
```

**Critério:**  
→ origem clara, rastreável e reproduzível

---

## 2. Versão e Estado do Código

```text
[ ] Versão / tag / commit atual identificado
[ ] Comparado com a última release disponível
[ ] Estado atual classificado:
    ( ) atualizado
    ( ) levemente defasado (aceitável)
    ( ) muito defasado (risco)
```

**Critério:**  
→ no máximo levemente defasado e com consciência do estado

---

## 3. Escopo de Suporte

```text
[ ] Tipo de build identificado:
    ( ) oficial
    ( ) fork / modificação
[ ] Verificado se está dentro do escopo de suporte do projeto
```

**Critério:**  
→ se for fork/modificação, uso consciente como ambiente controlado

---

## 4. Integridade da Instalação

```text
[ ] Instalação concluída sem erros críticos
[ ] Dependências resolvidas corretamente
[ ] Nenhum comportamento suspeito durante instalação
    (downloads inesperados, scripts não previstos, etc.)
```

**Critério:**  
→ instalação previsível e limpa

---

## 5. Comportamento em Runtime

```text
[ ] Executa apenas quando chamado (modo CLI controlado)
[ ] Não abre portas inesperadas
[ ] Não realiza chamadas externas sem comando explícito
[ ] Não executa ações automáticas fora do esperado
```

**Critério:**  
→ comportamento determinístico e sob controle do usuário

---

## 6. Verificação de Segurança Local

```text
[ ] Verificado por antivírus / Defender
[ ] Sem alertas críticos
[ ] Sem comportamento classificado como ameaça
```

**Critério:**  
→ ausência de alertas relevantes

---

## 7. Exposição de Dados

```text
[ ] Não envia dados automaticamente para serviços externos
[ ] Execução controlada via CLI
[ ] Integrações externas desativadas ou conscientemente habilitadas
```

**Critério:**  
→ fluxo totalmente controlado pelo usuário

---

## 8. Decisão Operacional

Selecionar uma opção:

```text
( ) Aprovado para uso diário local
( ) Aprovado com ressalvas (uso controlado)
( ) Somente para ambiente de teste
( ) Rejeitado / requer substituição
```

---

## 9. Política de Atualização

```text
[ ] Frequência de revisão definida (ex: mensal)
[ ] Atualizações não são automáticas
[ ] Novas versões são testadas antes de uso no fluxo principal
```

**Critério:**  
→ atualização controlada e consciente

---

# Interpretação Operacional

**Aprovado para uso diário**  
→ pode integrar ao fluxo principal

**Aprovado com ressalvas**  
→ usar com restrições:
- sem automação
- sem integração profunda
- validação manual de outputs

**Somente teste**  
→ não utilizar como base do workflow principal

---

# Princípio de Segurança

> Não confiar porque funciona.  
> Confiar porque foi validado.

---

# Observação

Este checklist é uma validação mínima de confiança.  
Não substitui auditoria completa de segurança, mas é suficiente para uso controlado em ambiente local.
