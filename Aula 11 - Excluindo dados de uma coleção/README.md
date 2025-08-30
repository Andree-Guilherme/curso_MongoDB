# 🗑️ Excluindo Documentos em uma Coleção via Shell

---

### 1️⃣ Excluindo um documento

<pre><code>db.&lt;collection&gt;.deleteOne(
   {"&lt;key&gt;": "&lt;value&gt;"}
);
</code></pre>

**Passos:**
1. Substitua `<collection>` pelo nome da collection.
2. No filtro (`{"<key>": "<value>"}`), especifique o campo e valor que deseja localizar.
3. O `deleteOne` remove **apenas o primeiro documento encontrado** que atenda ao critério.
4. O MongoDB retorna a contagem de documentos removidos (`deletedCount: 1` ou `0`).

---

### 2️⃣ Excluindo vários documentos

<pre><code>db.&lt;collection&gt;.deleteMany(
   {"&lt;key&gt;": "&lt;value&gt;"}
);
</code></pre>

**Passos:**
1. Substitua `<collection>` pelo nome da collection.
2. Defina o filtro para escolher **quais documentos** serão removidos.
3. O `deleteMany` remove **todos os documentos** que correspondem ao critério.
4. O MongoDB retorna a quantidade de documentos removidos (`deletedCount: X`).

---

> ⚠️ **Atenção:** Se o filtro for `{}`, o comando remove **todos os documentos da collection**, mas a collection em si permanece vazia.
