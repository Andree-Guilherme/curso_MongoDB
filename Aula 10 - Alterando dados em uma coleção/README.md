# 🔄 Alterando Dados em uma Coleção

[MATERIAL DE APOIO: Métodos de Atualização do MongoDB](https://www.mongodb.com/docs/manual/reference/update-methods/)

---

## 🔹 Métodos de Atualização

### 1️⃣ updateOne – Atualiza um único documento

**Descrição:** Encontra o **primeiro** documento que corresponde ao filtro e atualiza seus dados.

<pre><code>db.&lt;collection&gt;.updateOne(
    { "&lt;key&gt;": &lt;value&gt; }, // Filtro para encontrar o documento
    { 
        $set: { 
            "&lt;key&gt;": &lt;newValue&gt; // Operador de atualização
        } 
    }
)</code></pre>

**Passos:**
1.  No primeiro objeto, defina o **filtro** para localizar o documento.
2.  No segundo objeto, use o operador `$set` para definir o(s) campo(s) e seu(s) novo(s) valore(s).
3.  Apenas o **primeiro documento** que corresponder ao filtro será atualizado.

---

### 2️⃣ updateMany – Atualiza múltiplos documentos

**Descrição:** Encontra **todos** os documentos que correspondem ao filtro e atualiza seus dados.

<pre><code>db.&lt;collection&gt;.updateMany(
    { "&lt;key&gt;": &lt;value&gt; }, // Filtro para encontrar os documentos
    { 
        $set: { 
            "&lt;key&gt;": &lt;newValue&gt;
        } 
    }
)</code></pre>

**Passos:**
1.  Defina o **filtro** para localizar todos os documentos desejados.
2.  Use `$set` para definir os campos a serem atualizados.
3.  **Todos os documentos** que corresponderem ao filtro serão atualizados.

---

### 3️⃣ updateMany – Adicionando um novo campo a todos os documentos

**Descrição:** Utiliza um filtro vazio para selecionar todos os documentos da coleção e adicionar um novo campo a eles.

<pre><code>db.&lt;collection&gt;.updateMany(
    {}, // Filtro vazio para selecionar todos
    { 
        $set: { 
            "novoCampo": "valor" 
        } 
    }
)</code></pre>

**Passos:**
1.  Use um filtro vazio `{}` para selecionar **todos os documentos**.
2.  No `$set`, defina o **novo campo** e o valor que será adicionado.
3.  O novo campo será adicionado a **todos os documentos** da coleção.

---

### 4️⃣ updateOne com ObjectId – Atualizando um registro específico

**Descrição:** A forma mais segura de atualizar um único documento, usando seu `_id` único.

<pre><code>// 1. Guarde o ObjectId em uma variável
var idParaAtualizar = ObjectId('&lt;id_do_documento&gt;');

// 2. Use a variável no filtro do updateOne
db.&lt;collection&gt;.updateOne(
    { "_id": idParaAtualizar },
    {
        $set: { "&lt;key&gt;": "&lt;novo_valor&gt;" }
    }
);

// 3. (Opcional) Verifique a alteração
db.&lt;collection&gt;.find({ "_id": idParaAtualizar });
</code></pre>

**Passos:**
1.  Crie uma variável para armazenar o `ObjectId` do documento.
2.  Use esta variável no filtro `{ "_id": variavel }` para garantir a seleção do documento exato.
3.  Defina as alterações com `$set`.

---

## 📝 Gerenciando Variáveis no Mongo Shell

O Mongo Shell permite o uso de variáveis para facilitar as operações.

### Variáveis Declaradas (`var`, `let`, `const`)
> Estas variáveis são parte do escopo do shell e não podem ser removidas com `delete`.

*   **Listar variáveis:** `Object.keys(this)`
*   **Verificar tipo:** `typeof nomeDaVariavel`
*   **Limpar valor:** `nomeDaVariavel = undefined;` (atribui o valor `undefined` à variável, mas não a remove)

### Variáveis Globais (sem `var`, `let` ou `const`)
> Variáveis criadas por atribuição direta (`nome = valor`) podem ser removidas.

*   **Criar variável global:** `minhaVariavel = "teste"`
*   **Remover variável:** `delete this.minhaVariavel`
