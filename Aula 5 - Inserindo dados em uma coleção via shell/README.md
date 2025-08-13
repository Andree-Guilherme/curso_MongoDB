# Inserindo dados em uma coleção via shell

([MATERIAL DE APOIO] Tipos de JSON)[https://www.mongodb.com/pt-br/docs/manual/reference/bson-types/]

* Existem 2 comando para inserir dados

1. Abra o CMD ou terminal
2. Conecte-se ao MongoDB usando `mongosh` ou a URI do seu cluster no Atlas
3. Selecione o banco de dados com:
`use <nome_do_banco>`
4. Para inserir apenas um registro, utilize:
`db.<nome_da_collection>.insertOne({"<nome_do_campo>": <valor>, <"nome_do_campo">: <valor>})`
   1. Serve para inserir apenas um valor
5. Para inserir vários registros de uma vez, utilize:
`db.<nome_da_collection>.insertMany([{"<nome_do_campo">: <valor>},{"<nome_do_campo": <valor>}])`
   1. Serve para inserir mais de um valor — os documentos ficam dentro de um array
   2. Ao acessar o MongoDB Compass, irão aparecer 2 ou mais registros individualmente


* Ao acessar o mongodb compass, selecionar o banco desejado e clicar em __> _Open MongoDB shell__ sera aberto o shell diretamente no compass podendo fazer as mesmas operacoes que seria via terminal cmd