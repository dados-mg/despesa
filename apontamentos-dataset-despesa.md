# Apontamentos dataset despesa

1. como estava no CKAN antigo:

* 16 tabelas-dimensão e 1 fato:

	tempo_diario
	funcao
	subfuncao
	acao
	programa
	procedencia
	empenho
	fonte
	modalidade_aplic
	categ_econ
	grupo_desp
	elemento_des
	item_desp
	favorecido
	tipo_documento = nomes de valores possíveis com abreviações (op pendente) = VERIFICAR COMPLETUDE E CLAREZA DOS CONCEITOS DESSES VALORES POSSÍVEIS
	unidade_orc = 2 pares de colunas id/nome para adminisrtação e grupo de administração (ex.: autarquias e fundações == fundação), SEM NECESSIDADE DA QUASE DUPLICIDADE = EXISTE ESSE FILTRO NA INTERFACE??
	ft-despesa

	* adicionar funcao no datapackage, corrigir name unidade-prcamentaria, 
	* verificar descrição (fonte = verificar tooltip tabela mapa e armazém) de cada tabela e fazer de cada coluna
	* verificar conceitos e valores aplicáveis às colunas 'sqa', das tabelas-fato, tp_documento e unidade_orc

2. mapa portal

	* campos que não estão na consulta avançada do portal: fonte e tipo_documento

3. GRP de-para


4. fontes para versão simplificada da despesa: transparencia internacional, OKBR, [card com padrões Portugal e Buenos Aires])(https://trello.com/c/JIRHfLlD)



* 