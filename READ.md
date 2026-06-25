# ClearBank — Análise Financeira com Python

Projeto de análise de transações bancárias desenvolvido como desafio final da pós-graduação em Análise de Dados.

## Sobre o projeto

A empresa fictícia **ClearBank** exporta mensalmente o histórico de transações dos clientes em um arquivo CSV com problemas frequentes: campos vazios, valores inválidos e datas mal formatadas.

Este notebook Python resolve esse problema ao:

- Ler e validar o arquivo `transacoes.csv`
- Descartar registros inválidos e reportar o total
- Calcular métricas financeiras mensais (crédito, débito, saldo, média)
- Identificar transações suspeitas (acima de R$ 10.000)
- Exportar os resultados em `relatorio.json`

## Arquivos do projeto

| Arquivo | Descrição |
|---|---|
| `desafio-final.ipynb` | Notebook principal com todo o código |
| `transacoes.csv` | Dados de entrada (20 registros válidos + 5 inválidos) |
| `relatorio.json` | Gerado automaticamente ao executar o notebook |

## Como executar

### No Google Colab
1. Faça upload dos arquivos `desafio-final.ipynb` e `transacoes.csv`
2. Abra o notebook e clique em `Runtime → Run all`

### No VS Code (local)
1. Instale Python e a extensão Jupyter
2. Abra a pasta do projeto no VS Code
3. Abra `desafio-final.ipynb` e clique em `Run All`

## Saída gerada

O notebook exibe no terminal um relatório mensal formatado e gera o arquivo `relatorio.json` com a estrutura:

```json
{
  "gerado_em": "2026-06-25",
  "total_transacoes_validas": 20,
  "total_transacoes_invalidas": 5,
  "resumo_mensal": { ... },
  "transacoes_suspeitas": [ ... ]
}