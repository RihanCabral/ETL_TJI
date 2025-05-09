API – Taxas de Juros de Operações de Crédito (Banco Central do Brasil)

Descrição
Esta API fornece as taxas médias de juros praticadas pelas instituições financeiras em diversas modalidades de crédito, calculadas a partir dos últimos 5 dias úteis ou por mês de referência. Os dados são públicos e disponibilizados pelo Banco Central do Brasil através do protocolo OData.

URL Base
https://olinda.bcb.gov.br/olinda/servico/taxaJuros/versao/v2/odata/

Recursos disponíveis
1. TaxasJurosDiariaPorInicioPeriodo
Taxas médias de juros praticadas pelas instituições nos últimos 5 dias úteis.

2. TaxasJurosMensalPorMes
Taxas médias de juros por mês de referência, agrupadas por instituição e modalidade de crédito.

Parâmetros OData disponíveis
Parâmetro	Descrição
$format	Define o formato da resposta: json, xml, csv, etc.
$filter	Aplica filtros aos dados (ex: modalidade eq 'Crédito Pessoal').
$select	Seleciona colunas específicas.
$orderby	Ordena os dados por campos definidos (ex: dataInicioPeriodo desc).
$top	Limita o número de registros retornados.
$skip	Ignora um número definido de registros (paginação).

Dicionário de Dados
Recurso: TaxasJurosDiariaPorInicioPeriodo
Campo	Tipo	Descrição
dataInicioPeriodo	date	Data de início do período (últimos 5 dias úteis).
codInstituicao	integer	Código da instituição financeira.
nomeInstituicao	string	Nome da instituição financeira.
codModalidade	integer	Código da modalidade de crédito.
modalidade	string	Tipo da modalidade (ex: Crédito Pessoal, Financiamento Imobiliário).
taxaJuros	float	Taxa média de juros (em % ao ano) no período.

Recurso: TaxasJurosMensalPorMes
Campo	Tipo	Descrição
mesReferencia	string	Mês de referência no formato YYYY-MM.
codInstituicao	integer	Código da instituição financeira.
nomeInstituicao	string	Nome da instituição financeira.
codModalidade	integer	Código da modalidade de crédito.
modalidade	string	Descrição da modalidade de crédito.
taxaJuros	float	Taxa média de juros (em % ao ano) do mês de referência.
