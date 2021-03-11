# Reunião GRP Isabella e DCTA - 2021-03-11


* Restos a Pagar - Campo Tipo de Empenho e Número do empenho RP processado

Em uma mesma consulta, itens dimensionais conversam com institucional. União (símbolo da intersecção da ferramenta BO) pode ser feita entre consultas. Para fazer o cruzamento é necessário auxiliares de consulta. Luiz vai construir base e não a camada semântica, então a construção que a DCTA indicar será livre. (ex.: inscrição de restos a pagar tem indicativos dos documentos do empenho no SIAFI). Luiz consegue cruzar com um campo-chave, e DCTA precisa fazer consultas para conferir o que Luiz construiu. Inscrição do empenho ou inscrição da OLP = montar consulta resgatando os documentos de trás para frente, usando a união (mas auxiliares da consulta ainda não estão disponibilizados).

Auxiliar = recuperar dado do tipo de empenho, que está no documento do empenho (auxiliar1 deve ser movido para a primeira consulta; na segunda consulta, ao ir na tabela, completando valores que seriam nulos para a segunda, trazer só o tipo de empenho; os demais são preenchidos pelos auxiliares)

OLP = RPP (ainda que tenha empenho de origem)

Empenho = RPNP


* Restos a Pagar - Valor Liquidado

Despesa liquidada bruta (documento de liquidação, estático) > despesa liquidada (fórmula: liquidado bruto - anulação bruta) > despesa liquidada a pagar (fórmula: liquidação - anulação - pago)

O que a DCTA evidencia? a pagar não evidencia, somente liquidação total

Portal da Transparência tem que estar com a mesma fórmula que o RREO e documentos de referência para o Tesouro Nacional (p. ex. despesa liquidada tem que bater)




## Dicas gerais e encaminhamentos

Dicionários de dados: verificar o manual (versão jan/21 salvo na pasta do repo)

Dica da Isabella: entrar no transacional, resumo do empenho, rodar uma consulta fixa daquele empenho no armazém; no GRP tem a movimentação do empenho

Maio: passo a passo com exemplos reais de documentos preenchidos pelos bombeiros no GRP

Agosto/setembro: rodada com o grupo da Contadoria