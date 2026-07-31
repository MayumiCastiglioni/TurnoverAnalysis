---
name: turnover-vault
description: Mantém o vault de contexto do projeto Turnover (decisions e infos) em Análise inicial/vault/. Use ao iniciar sessões no TurnoverAnalysis, ao receber e-mails ou contexto do RH, ao tomar decisões analíticas, ou quando o usuário pedir para documentar no ARP/vault.
---

# Turnover Vault

## Instrução fixa (executar sempre neste projeto)

Ao **iniciar** ou **encerrar** trabalho no TurnoverAnalysis:

1. Ler `Análise inicial/vault/README.md` e os arquivos recentes em `decisions/` e `infos/`
2. Extrair da conversa atual: decisões, pedidos do RH, limitações de dados, descobertas analíticas
3. Atualizar ou criar entradas no vault **antes de finalizar** a sessão
4. Referenciar IDs (INFO-XXX, DEC-XXX) nas respostas ao usuário quando relevante

## Localização

```
Análise inicial/vault/
├── README.md
├── infos/       # Contexto, e-mails, descobertas
└── decisions/   # Decisões analíticas e de projeto
```

## O que registrar

| Tipo | Pasta | Quando |
|------|-------|--------|
| INFO | `vault/infos/` | Contexto, e-mails, metadados de bases, descobertas do discovery |
| DEC | `vault/decisions/` | Escolhas analíticas: universo, grain, filtros, chaves de join |

## Templates

### INFO-XXX (`vault/infos/NNN-titulo.md`)

```markdown
# INFO-XXX: Título

**Data:** YYYY-MM-DD
**Fonte:** origem (e-mail, notebook, conversa)

## Conteúdo
[fatos, contexto, números]

## Impacto na análise
[o que muda ou restringe a análise]
```

### DEC-XXX (`vault/decisions/NNN-titulo.md`)

```markdown
# DEC-XXX: Título

**Data:** YYYY-MM-DD
**Status:** Proposto | Aceito | Substituído

## Contexto
[por que a decisão foi necessária]

## Decisão
[o que foi escolhido]

## Consequências
[impactos práticos]

## Alternativas rejeitadas
[o que foi descartado e por quê]
```

## Regras

- Numeração sequencial por pasta: `001-titulo-curto.md`
- **Nunca sobrescrever** entradas existentes; criar novo arquivo se a decisão mudar
- Atualizar o índice em `vault/README.md` ao adicionar entradas
- Não registrar código temporário ou outputs de notebook sem interpretação

## Não registrar

- Explorações ad hoc sem conclusão
- Duplicatas de informação já documentada (referenciar o INFO/DEC existente)
