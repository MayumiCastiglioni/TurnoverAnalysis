# INFO-004: Discovery Inicial

**Data:** 2026-07-31  
**Fonte:** `analise_inicial.ipynb`

## FtDemitidosTurnoverRH

| Métrica | Valor |
|---------|-------|
| Registros | 20.587 |
| IDs únicos (`nIdPessoa`) | 19.953 |
| Registros duplicados por ID | 634 |
| Pessoas com >1 desligamento | 604 |
| Período | 2016–2024 |

**Iniciativa da demissão:**
- Voluntário: 14.201
- Involuntário: 6.386

## FtFuncionarioRH_amostra

| Métrica | Valor |
|---------|-------|
| Registros | 24.000 |
| IDs únicos | 24.000 |
| Período | 2016–2024 |

**Situação (principais):**
- Demitido: 19.639
- Ativo: 3.797
- Outros (férias, afastamentos etc.): ~564

## Cruzamento por `nIdPessoa`

| Métrica | Valor |
|---------|-------|
| IDs em comum | 17.939 |
| % demitidos na amostra | **89,9%** |
| % amostra em demitidos | 74,7% |
| Só em Demitidos | 2.014 |
| Só em Funcionários | 6.061 |

## Impacto na análise

- Overlap de ~90% confirma viabilidade do universo analítico
- 2.014 demitidos fora da amostra devem ser documentados como limitação
- 604 pessoas com múltiplos desligamentos exigem decisão de grain (ver DEC-001)
