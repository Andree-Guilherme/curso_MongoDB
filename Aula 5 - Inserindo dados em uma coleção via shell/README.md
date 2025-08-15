# Inserindo dados em uma coleção via shell

(MATERIAL DE APOIO: Tipos de JSON)(https://www.mongodb.com/pt-br/docs/manual/reference/bson-types/)

### Passo a passo

**1. Abra o CMD:**  
`mongosh`

> _ou use a URI do seu cluster Atlas_

**2. Conecte ao MongoDB:**  
`use <database>`

**Inserindo um registro:**  
`db.<collection>.insertOne({`
   `"<key>": <value>,`
   `"<key>": <value> `
`});`

> _útil para inserir apenas um documento por vez_

**Inserindo vários registros:**  
`db.<collection>.insertMany([`
   `{"<nome_do_campo>": <valor>},`
   `{"<nome_do_campo>": <valor>}`
`])`

> _serve para inserir múltiplos documentos de uma vez (dentro de um array)_

---

* No MongoDB Compass, é possível abrir o shell integrado em `> Open MongoDB shell` e executar os mesmos comandos