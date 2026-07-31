# DEC-001: Definição do Universo Analítico

**Data:** 2026-07-31  
**Status:** Aceito (provisório)

## Contexto

Cruzamento entre `FtDemitidosTurnoverRH` e `FtFuncionarioRH_amostra` via `nIdPessoa` revelou 89,9% de overlap (17.939 IDs em comum).

## Decisão

Trabalhar com a **interseção das duas bases** (17.939 IDs) como universo analítico inicial.

## Consequências

- Universo suficiente para modelagem e perfilamento inicial
- ~10% dos demitidos (2.014 IDs) ficam fora — documentar como limitação
- 604 pessoas têm mais de um registro de desligamento — **grain pendente** (pessoa vs evento)
- 6.061 IDs só na amostra de funcionários (ativos ou demitidos não capturados na base de turnover) ficam fora do escopo inicial focado em desligamentos

## Alternativas rejeitadas

| Alternativa | Motivo |
|-------------|--------|
| Usar só demitidos | Perde histórico mensal pré-desligamento |
| Usar só funcionários | Perde motivo, tipo e iniciativa de demissão |
| Exigir 100% de overlap | Inviable com dados atuais; 90% é aceitável |

## Próximo passo

Definir grain (DEC-003 pendente) e validar se os 2.014 IDs ausentes têm padrão sistemático (ex.: filial, ano).
