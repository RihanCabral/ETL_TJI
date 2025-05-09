{
  "api_nome": "Taxas de Juros de Operações de Crédito",
  "descricao": "API do Banco Central que fornece as taxas médias de juros praticadas pelas instituições financeiras em diversas modalidades de crédito, com dados diários (últimos 5 dias úteis) e mensais.",
  "url_base": "https://olinda.bcb.gov.br/olinda/servico/taxaJuros/versao/v2/odata/",
  "formatos_disponiveis": ["json", "xml", "csv", "html"],
  "parametros_odata": {
    "$format": "Define o formato de resposta (ex: json, xml)",
    "$filter": "Filtra registros por condição (ex: modalidade eq 'Crédito Pessoal')",
    "$select": "Seleciona colunas específicas",
    "$orderby": "Ordena os dados (ex: dataInicioPeriodo desc)",
    "$top": "Define o número máximo de registros retornados",
    "$skip": "Define o número de registros a ignorar (paginação)"
  },
  "recursos": [
    {
      "nome": "TaxasJurosDiariaPorInicioPeriodo",
      "descricao": "Taxas médias de juros por instituição nos últimos 5 dias úteis",
      "dicionario_dados": [
        {
          "campo": "dataInicioPeriodo",
          "tipo": "date",
          "descricao": "Data de início do período (últimos 5 dias úteis)"
        },
        {
          "campo": "codInstituicao",
          "tipo": "integer",
          "descricao": "Código da instituição financeira"
        },
        {
          "campo": "nomeInstituicao",
          "tipo": "string",
          "descricao": "Nome da instituição financeira"
        },
        {
          "campo": "codModalidade",
          "tipo": "integer",
          "descricao": "Código da modalidade de crédito"
        },
        {
          "campo": "modalidade",
          "tipo": "string",
          "descricao": "Descrição da modalidade de crédito"
        },
        {
          "campo": "taxaJuros",
          "tipo": "float",
          "descricao": "Taxa média de juros no período (em % ao ano)"
        }
      ]
    },
    {
      "nome": "TaxasJurosMensalPorMes",
      "descricao": "Taxas médias de juros por instituição por mês de referência",
      "dicionario_dados": [
        {
          "campo": "mesReferencia",
          "tipo": "string",
          "descricao": "Mês de referência no formato YYYY-MM"
        },
        {
          "campo": "codInstituicao",
          "tipo": "integer",
          "descricao": "Código da instituição financeira"
        },
        {
          "campo": "nomeInstituicao",
          "tipo": "string",
          "descricao": "Nome da instituição financeira"
        },
        {
          "campo": "codModalidade",
          "tipo": "integer",
          "descricao": "Código da modalidade de crédito"
        },
        {
          "campo": "modalidade",
          "tipo": "string",
          "descricao": "Descrição da modalidade de crédito"
        },
        {
          "campo": "taxaJuros",
          "tipo": "float",
          "descricao": "Taxa média de juros no mês (em % ao ano)"
        }
      ]
    }
  ]
}
