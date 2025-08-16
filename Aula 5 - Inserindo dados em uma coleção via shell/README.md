# Inserindo dados em uma coleção via shell

(MATERIAL DE APOIO: Tipos de JSON)[https://www.mongodb.com/pt-br/docs/manual/reference/bson-types]

### Passo a passo

**1. Abra o CMD:**  
`mongosh`

> _ou use a URI do seu cluster Atlas_

<br>

**2. Conecte ao MongoDB:**  
`use <database>`

<br>

**Inserindo um registro:**  
<pre><code>db.&lt;collection&gt;.insertOne({
   "&lt;key&gt;": &lt;value&gt;,
   "&lt;key&gt;": &lt;value&gt;
});
</code></pre>

> _útil para inserir apenas um documento por vez_

<br>

**Inserindo vários registros:**  
<pre><code>db.&lt;collection&gt;.insertMany([
   {"&lt;key&gt;": &lt;value&gt;},
   {"&lt;key&gt;": &lt;value&gt;}
])
</code></pre>


> _serve para inserir múltiplos documentos de uma vez (dentro de um array)_

---


* No MongoDB Compass, é possível abrir o shell integrado em `> Open MongoDB shell` e executar os mesmos comandos
