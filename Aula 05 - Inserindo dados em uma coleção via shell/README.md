# 💻 Inserindo Dados em uma Coleção via Shell

[MATERIAL DE APOIO: Tipos de JSON](https://www.mongodb.com/pt-br/docs/manual/reference/bson-types)

---

## 🔹 Passo a passo

### 1️⃣ Abra o CMD

<pre><code>mongosh</code></pre>

**Passos:**
1. Abra o terminal ou CMD do seu sistema.
2. Digite `mongosh` para iniciar o MongoDB Shell.
3. Alternativamente, use a **URI do seu cluster Atlas** para conexão remota.

---

### 2️⃣ Conecte ao MongoDB

<pre><code>use &lt;database&gt;</code></pre>

**Passos:**
1. Substitua `<database>` pelo nome do banco de dados que deseja usar.
2. Este comando seleciona o banco de dados ativo para os próximos comandos.
3. Caso o banco não exista, ele será criado na primeira inserção.

---

### 3️⃣ Inserindo um registro

<pre><code>db.&lt;collection&gt;.insertOne({
   "&lt;key&gt;": &lt;value&gt;,
   "&lt;key&gt;": &lt;value&gt;
});
</code></pre>

**Passos:**
1. Substitua `<collection>` pelo nome da collection onde deseja inserir o documento.
2. Preencha os campos e valores dentro do objeto JSON.
3. Use `insertOne` para inserir **apenas um documento por vez**.
4. Após execução, o MongoDB retorna o **ID** gerado automaticamente para o documento.

---

### 4️⃣ Inserindo vários registros

<pre><code>db.&lt;collection&gt;.insertMany([
   {"&lt;key&gt;": &lt;value&gt;},
   {"&lt;key&gt;": &lt;value&gt;}
]);
</code></pre>

**Passos:**
1. Substitua `<collection>` pelo nome da collection.
2. Adicione múltiplos objetos JSON dentro do **array**.
3. Cada objeto representa um documento distinto.
4. `insertMany` insere **vários documentos de uma vez**.
5. O MongoDB retorna os IDs de todos os documentos inseridos.

---

> 💡 No MongoDB Compass, é possível abrir o **shell integrado** em `> Open MongoDB shell` e executar os mesmos comandos diretamente na interface gráfica.
