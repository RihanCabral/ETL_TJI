## API – Taxas de Juros de Operações de Crédito (Banco Central do Brasil)

**Formatos disponíveis:**  
- `json` (padrão)  
- `xml`  
- `text/csv`  
- `text/html`  

Fonte: [Portal de Dados Abertos do Banco Central](https://dadosabertos.bcb.gov.br/)

---

Parâmetros OData Comuns

| **Parâmetro** | **Tipo**  | **Descrição**                                                                 |
|---------------|-----------|------------------------------------------------------------------------------|
| `$format`     | texto     | Formato de saída (json, xml, csv, html).                                     |
| `$select`     | texto     | Seleção de propriedades a retornar (ex: nomeInstituicao, valor).              |
| `$filter`     | texto     | Filtro de entidades (ex: modalidade eq 'Crédito Pessoal').                    |
| `$orderby`    | texto     | Ordenação dos resultados (ex: dataInicioPeriodo desc).                        |
| `$top`        | inteiro   | Número máximo de registros retornados.                                       |
| `$skip`       | inteiro   | Número de registros a serem ignorados (para paginação).                      |

---

Dicionário de Dados

### 1. Recurso: `TaxasJurosDiariaPorInicioPeriodo`

Taxas médias **diárias** (últimos 5 dias úteis) para cada instituição e modalidade de crédito.

| **Campo**           | **Tipo**   | **Descrição**                                                                 |
|---------------------|------------|-------------------------------------------------------------------------------|
| `dataInicioPeriodo` | `date`     | Data de início do período de 5 dias úteis (formato YYYY-MM-DD).              |
| `codInstituicao`    | `integer`  | Código numérico da instituição financeira no sistema do Banco Central.       |
| `nomeInstituicao`   | `string`   | Nome oficial da instituição financeira.                                      |
| `codModalidade`     | `integer`  | Código da modalidade de crédito (ex: pessoal, imobiliário, empresarial).     |
| `modalidade`        | `string`   | Descrição da modalidade de crédito.                                          |
| `taxaJuros`         | `number`   | Taxa média de juros apurada no período, expressa em percentual (com encargos).|

Fonte: [Portal de Dados Abertos do Banco Central](https://dadosabertos.bcb.gov.br/)

---

### 2. Recurso: `TaxasJurosMensalPorMes`

Taxas médias **mensais** para cada instituição e modalidade de crédito.

| **Campo**         | **Tipo**   | **Descrição**                                                             |
|-------------------|------------|--------------------------------------------------------------------------|
| `mesReferencia`   | `string`   | Mês de referência da taxa, no formato YYYY-MM.                           |
| `codInstituicao`  | `integer`  | Código da instituição financeira.                                        |
| `nomeInstituicao` | `string`   | Nome da instituição financeira.                                          |
| `codModalidade`   | `integer`  | Código da modalidade de crédito.                                         |
| `modalidade`      | `string`   | Descrição da modalidade de crédito.                                      |
| `taxaJuros`       | `number`   | Taxa média de juros no mês de referência, expressa em percentual.       |

Fonte: [Portal de Dados Abertos do Banco Central](https://dadosabertos.bcb.gov.br/)
