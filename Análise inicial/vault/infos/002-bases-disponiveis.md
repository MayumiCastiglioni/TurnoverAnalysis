# INFO-002: Bases de Dados Disponíveis

**Data:** 2026-07-31  
**Fonte:** Pasta `Bases de Dados/`

## Bases principais (análise inicial)

| Arquivo | Descrição | Registros |
|---------|-----------|-----------|
| `FtDemitidosTurnoverRH.csv` | Eventos de desligamento | 20.587 |
| `FtFuncionarioRH_amostra.csv` | Painel mensal de colaboradores | 24.000 |

## Bases complementares

| Arquivo | Descrição |
|---------|-----------|
| `FtAbsenteismoMensalRH.csv` | Absenteísmo mensal |
| `FtAcidentesRH.csv` | Acidentes de trabalho |
| `FtHoraExtraRH.csv` | Horas extras |
| `FtHorasIrregularesRH.csv` | Horas irregulares |
| `FtMovimentoSalarialRH.csv` | Movimentação salarial |
| `MotivosDemitidos_referencia.csv` | Tabela de referência de motivos |

## Formato

- Separador: `;`
- Chave principal para join: `nIdPessoa`
- Período demitidos: 2016–2024
- Período funcionários (amostra): 2016–2024

## Colunas-chave

**Demitidos:** `nIdPessoa`, `cIniciativaDemissao`, `cDescricaoTipoDemissao`, `cDescricaoMotivoDemissao`, `cSecao`, `cCargo`, `nAno`, `dDataDemissao`, `dDataAdmissao`, variáveis demográficas

**Funcionários:** `nIdPessoa`, `cSituacao`, `dAnoMes`, `cSecao`, `cCargo`, `nTempoDeCasaAnos`, `nSalarioTotal`, variáveis demográficas
