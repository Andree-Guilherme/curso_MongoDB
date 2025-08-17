# 📌 MongoDB Update Operations Step-by-Step

### 1️⃣ updateOne – Atualiza apenas o primeiro registro encontrado

<pre><code>db.&lt;collection&gt;.updateOne(
    { "&lt;key&gt;": &lt;value&gt; },
    { 
        $set: { 
            "&lt;key&gt;": &lt;newValue&gt; 
        } 
    }
)</code></pre>

**Passos:**
1. Defina a **collection** que deseja atualizar.
2. No primeiro parâmetro, especifique o **filtro** `{ "<key>": <value> }` para localizar o registro
3. No segundo parâmetro, use `$set` para definir o novo valor da chave
4. Apenas o **primeiro registro** que corresponder ao filtro será atualizado

---

### 2️⃣ updateOne – Atualizando múltiplos campos do primeiro registro

<pre><code>db.&lt;collection&gt;.updateOne(
    { "&lt;key&gt;": &lt;value&gt; },
    { 
        $set: { 
            "&lt;key1&gt;": &lt;newValue1&gt;,
            "&lt;key2&gt;": &lt;newValue2&gt;
        } 
    }
)</code></pre>

**Passos:**
1. Escolha a **collection**.
2. Especifique o **filtro** no primeiro parâmetro
3. No `$set`, defina **vários campos** a serem atualizados
4. Apenas o **primeiro documento correspondente** será alterado

---

### 3️⃣ updateMany – Atualiza todos os registros que correspondem ao filtro

<pre><code>db.&lt;collection&gt;.updateMany(
    { "&lt;key&gt;": &lt;value&gt; },
    { 
        $set: { 
            "&lt;key1&gt;": &lt;newValue1&gt;,
            "&lt;key2&gt;": &lt;newValue2&gt;
        } 
    }
)</code></pre>

**Passos:**
1. Selecione a **collection**.
2. Defina o **filtro** `{ "<key>": <value> }` para escolher os documentos
3. No `$set`, inclua todos os campos que deseja atualizar
4. Todos os **documentos correspondentes** ao filtro serão atualizados

---

### 4️⃣ updateMany – Adicionando um novo campo a todos os registros

<pre><code>db.&lt;collection&gt;.updateMany(
    {},
    { 
        $set: { 
            "fieldName": fieldValue 
        } 
    }
)</code></pre>

**Passos:**
1. Selecione a **collection**.
2. Use `{}` como filtro para selecionar **todos os documentos**
3. No `$set`, defina o **novo campo** e o valor que será adicionado
4. Todos os documentos da collection receberão o **novo campo**

---

### 5️⃣ updateOne usando ObjectId – Atualizando um registro específico

<pre><code>var id = ObjectId('&lt;idregistro&gt;');

db.&lt;collection&gt;.updateOne(
    {"_id": id},
    {
        $set: {
            "&lt;key&gt;": "&lt;value&gt;"
        }
    }
);

db.&lt;collection&gt;.find(
    {"_id": id}
);</code></pre>

**Passos:**
1. Crie uma variável `id` usando `ObjectId('<idregistro>')`
2. Selecione a **collection**
3. Use `updateOne` com o filtro `{"_id": id}`
4. No `$set`, defina o campo e o valor que deseja atualizar
5. Use `find({"_id": id})` para **verificar o registro atualizado**

---

## 📝 Variáveis no contexto do Mongo Shell

> Variáveis criadas com `var`, `let` ou `const` não são apagáveis pois são **não configuráveis** no contexto global.

1. Listar todas variáveis no contexto global do shell:
   <pre><code>Object.keys(this)</code></pre>
2. Mostrar o tipo de variável:
   <pre><code>typeof &lt;var&gt;</code></pre>
3. Ver o valor da variável:
   <pre><code>&lt;var&gt;</code></pre>
4. Para apagar de forma “suja” a variável:
   <pre><code>&lt;var&gt; = undefined;</code></pre>

> Variáveis criadas sem declaração podem ser apagáveis.

1. Criar variável sem declaração:
   <pre><code>&lt;var&gt; = &lt;value&gt;</code></pre>
2. Apagar variável:
   <pre><code>delete this.<var>;</code></pre>