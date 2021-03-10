# Apontamentos dataset despesa

### macroetapas de organização do trabalho de análise e preparação:

* com o que temos atualmente (CKAN antigo/diagrama de relacionamento X Portal X armazám)

	a) todas as tabelas (dimensão e fato) estão representadas no datapackage/schema?
	
	b) há descrição dos nomes das tabelas e de suas colunas no tooltip do Portal/Armazém?
	
	c) os valores dos dados nas colunas expressam o que os conceitos querem dizer?
	
	d) as propriedades dos valores podem ser expressas no datapackage/schema (padrões de codificação como 
	número de algarismos tipo minLenght, maxLenght e range)?
	
	e) os valores, quando reunidos por tabela dinâmica e procv, levam a um resultado esperado e coerente (com os do Portal?)
	
	f) a consulta e download dos arquivos é prática (tamanho, leiaute)?

* com o GRP:

g) como fazer refletir as atuais descrições de metadados para o GRP?

h) é preciso haver mudança de leiaute e/ou partição de arquivos?

* bônus (para o futuro): é possível pensar uma forma de consulta simplificada, a partir dos padrões e sugestões de entidades de transparência?  

### mapeamento e análise:

1. como estava no CKAN antigo:

* 16 tabelas-dimensão e 1 fato:

	1.tempo_diario
	
	2.funcao_desp
	
	3.subfuncao_desp
	
	4.acao
	
	5.programa
	
	6.procedencia
	
	7.empenho
	
	8.fonte
	
	9.modalidade_aplic
	
	10.categ_econ
	
	11.grupo_desp
	
	12.elemento_des
	
	13.item_desp
	
	14.favorecido
	
	15.tipo_documento 
	
	16.unidade_orc
	
	ft-despesa

	* 1.1. [v] corrigir ``name`` na tabela ``unidade-prcamentaria``, 
	
	* 1.2. 

		[ ] verificar descrição (fonte = verificar tooltip tabela mapa e armazém) de cada tabela e fazer de cada coluna = FALTA TABELA ``empenho``

		[ ] verificar a que correspondem os algarismos 0 e 9 na tabela de categoria econômica, previsão no Portal, no Armazém e no GRP
			

		[v] descrição da subfunção modificada: 'identifica a natureza básica das ações que se aglutinam **em funções**' em vez de 'identifica a natureza básica das ações que se aglutinam **em torno de** funções'

		[ ] coluna ``mes`` da tabela ``tempo_diario`` não apresenta dois algarismos para os meses de janeiro a setembro (ex. 1 e 9 em vez de 01 e 09)

		[v] qual a descrição da ``tipo_documento``?? descrição sugerida: _´tipo do documento que identifica as operações possíveis no processo de execução da despesa´_

		[ ] ``tipo_documento``: nomes de valores possíveis com abreviações (op pendente) = VERIFICAR COMPLETUDE E CLAREZA DOS CONCEITOS DESSES VALORES POSSÍVEIS

		[ ] ``unidade_orc``: 2 pares de colunas id/nome para adminisrtação e grupo de administração (ex.: autarquias e fundações == fundação), SEM NECESSIDADE DA QUASE DUPLICIDADE = EXISTE ESSE FILTRO NA INTERFACE??

		[v] ``unidade_orc``: adição da descrição dos nomes das colunas ``grupo_administracao`` e ``administracao`` (categoria de pessoa jurídica)

		[ ] ``favorecido``: não há uma coluna para o nome que corresponde ao tipo de documento (p. ex., identidade, cpf, cnpj, passaporte, etc)

		[ ] passar misingValues para colunas correspondentes, em vez de deixar constar nos arquivos dos recursos como um todo

	- padrão de descrição: 

		tooltip Portal na propriedade 'description' das colunas 'name' e da propriedade 'description' dos recursos das tabelas-dimensão;

		listagem dos valores possíveis nas colunas de 'código', quando a listagem for pequena, e descrição do padrão (p. ex. número de algarismos dos códigos, quando a listagem for grande) = NÃO É UMA BOA PRÁTICA, está sendo feita como experiência pessoal para verificação da variabilidade dos códigos ao longo dos anos e da sua manutenção no GRP (a rigor, a mesma regra descritiva deve ser aplicada para todas as colunas de código, na notação exemplificada na pripriedade ``pattern``em [csv lint example](https://csvlint.io/schemas/530b1eb763737676e93c0000)) = PODE SER UM ISSUE  

		a descrição que consta no tooltip da ``procedencia`` ou IPU pode ser confundida com a descrição da fonte ou classificação da despesa: _"identifica a origem e a utilização dos recursos"_

	* [ ] verificar conceitos e valores aplicáveis à coluna 'sqa' da ``tabela-fato``

2. mapa portal

	* campos que não estão na consulta avançada do portal: fonte e tipo_documento

3. GRP de-para

3.1. Campos adicionais nas tabelas: representar exatamente como estão ou haverá grau de liberdade para definição de quantas e quais serão as colunas das tabelas dimensão dos novos conjuntos espelhados no GRP? Exemplo: ver tabela dm-unidade-orcamentaria

3.2. Como o 'contexto' afetará as decisões da questão 3.1. Exemplo: como ficará a tabela anterior 'dm-tempo-diario'? A nova consulta 'exercício' exige a seleção de um contexto para ser gerada (lançamento contábil, saldo contábil, despesa anulação, despesa empenhada, despesa liquidada, FINANCEIRA, PROGRAMAÇÃO, RECEITA, RESTOS A PAGAR )


4. fontes para versão simplificada da despesa: transparencia internacional, OKBR, [card com padrões Portugal e Buenos Aires])(https://trello.com/c/JIRHfLlD)



* referências:

	- [dicionário de dados do portal de Curitiba](https://mid.curitiba.pr.gov.br/dadosabertos/BaseReceitaDespesa/2016-04-07_Despesas_-_Dicionario_de_Dados.xlsx) 

	- [dicionário de dados do portal de Alagoas](http://transparencia.al.gov.br/portal/download-de-dados/despesas/comparativo-de-despesa)