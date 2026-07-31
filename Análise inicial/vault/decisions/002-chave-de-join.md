# DEC-002: Chave de Join entre Bases

**Data:** 2026-07-31  
**Status:** Aceito

## Contexto

Duas bases principais com granularidades diferentes:
- **Demitidos:** 1 registro por evento de desligamento (podem haver múltiplos por pessoa)
- **Funcionários:** 1 registro por pessoa-mês (painel)

## Decisão

Usar `nIdPessoa` como chave primária de join entre todas as bases do projeto.

## Consequências

- Join simples e consistente across bases
- Ao cruzar demitidos × funcionários, atentar para duplicidade (634 registros duplicados em demitidos)
- Joins com bases complementares (absenteísmo, horas extras etc.) também devem usar `nIdPessoa`

## Alternativas rejeitadas

| Alternativa | Motivo |
|-------------|--------|
| `nChapa` / `cChapa` | Pode variar entre coligadas; menos estável |
| Combinação coligada + chapa | Complexidade desnecessária; `nIdPessoa` já é único |

## Validação

- Demitidos: 19.953 IDs únicos em 20.587 registros
- Funcionários: 24.000 IDs únicos (sem duplicata na amostra)
- Interseção: 17.939 IDs (89,9% dos demitidos)
