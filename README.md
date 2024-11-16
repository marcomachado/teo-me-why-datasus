# Dados de Internações DATASUS (teomewhy)

## Sistema Saúde Datasus TeoMeWhy
	 - análise de internações
	 - identificação de dados
	 - RAW: 
		 - converter dados para CSV: datasus usa formato próprio (dbc -> csv)
		 - tabela sem chave-primária (formação de chave primária a partir de conjunto de campos)
	 - BRONZE:
		 - envio para BD no Delta Lake
		 - dados formato parquet
		 - cópia do delta (dados modificados - ano/mês)
		 - operação de upsert (update ou insert)
