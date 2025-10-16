# 🗑️ Excluindo Documentos de uma Coleção

[MATERIAL DE APOIO: db.collection.deleteOne()](https://www.mongodb.com/docs/manual/reference/method/db.collection.deleteOne/)
[MATERIAL DE APOIO: db.collection.deleteMany()](https://www.mongodb.com/docs/manual/reference/method/db.collection.deleteMany/)

---

Este guia explica como remover documentos de uma coleção usando os comandos `deleteOne` and `deleteMany` no Mongo Shell.

## 🔹 Comandos de Exclusão

### 1️⃣ deleteOne
**Descrição:** Remove o **primeiro** documento que corresponde ao filtro especificado.

**Uso:**
1.  Especifique um **filtro** para localizar o documento que deseja remover.
2.  O comando irá parar após remover o primeiro documento encontrado.
3.  O resultado da operação mostrará `deletedCount: 1` se um documento for removido.

**Exemplo:** Para remover o primeiro usuário com o status "INATIVO":
<pre><code>db.users.deleteOne({ "status": "INATIVO" });
</code></pre>

### 2️⃣ deleteMany
**Descrição:** Remove **todos** os documentos que correspondem ao filtro especificado.

**Uso:**
1.  Especifique um **filtro** para localizar os documentos que deseja remover.
2.  Todos os documentos que atenderem ao critério serão removidos.
3.  O resultado mostrará o número total de documentos removidos em `deletedCount`.

**Exemplo:** Para remover todos os produtos com quantidade em estoque igual a 0:
<pre><code>db.products.deleteMany({ "estoque": 0 });
</code></pre>

---

> ⚠️ **Cuidado:** Usar `deleteMany` com um filtro vazio (`{}`) removerá **TODOS** os documentos da coleção. A coleção continuará a existir, mas ficará vazia. Use com extrema cautela!
> <pre><code>// CUIDADO: ISSO APAGA TUDO DA COLEÇÃO 'logs'
db.logs.deleteMany({});
</code></pre>

> 💡 **Excluindo via Compass:** Na interface gráfica, você pode passar o mouse sobre um documento e clicar no **ícone de lixeira (🗑️)** para removê-lo individualmente.