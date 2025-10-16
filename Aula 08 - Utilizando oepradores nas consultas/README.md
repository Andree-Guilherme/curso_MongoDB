# ⚙️ Utilizando Operadores nas Consultas

[MATERIAL DE APOIO: Operadores de Consulta (Query Operators)](https://www.mongodb.com/pt-br/docs/manual/reference/operator/query/)

---

Operadores de consulta estendem a funcionalidade das buscas no MongoDB, permitindo criar filtros complexos e poderosos. Eles são sempre prefixados com o símbolo `$`.

## 🔹 Operadores de Comparação

### 1️⃣ $eq (Equal)
**Descrição:** Encontra documentos onde o valor de um campo é **igual** ao valor especificado.
<pre><code>db.inventory.find({ "qty": { $eq: 20 } })</code></pre>

### 2️⃣ $gt (Greater Than)
**Descrição:** Encontra documentos onde o valor do campo é **maior que** o valor especificado.
<pre><code>db.inventory.find({ "qty": { $gt: 20 } })</code></pre>

### 3️⃣ $gte (Greater Than or Equal)
**Descrição:** Encontra documentos onde o valor do campo é **maior ou igual a** o valor especificado.
<pre><code>db.inventory.find({ "qty": { $gte: 20 } })</code></pre>

### 4️⃣ $lt (Less Than)
**Descrição:** Encontra documentos onde o valor do campo é **menor que** o valor especificado.
<pre><code>db.inventory.find({ "qty": { $lt: 20 } })</code></pre>

### 5️⃣ $lte (Less Than or Equal)
**Descrição:** Encontra documentos onde o valor do campo é **menor ou igual a** o valor especificado.
<pre><code>db.inventory.find({ "qty": { $lte: 20 } })</code></pre>

### 6️⃣ $ne (Not Equal)
**Descrição:** Encontra documentos onde o valor do campo é **diferente** do valor especificado.
<pre><code>db.inventory.find({ "qty": { $ne: 20 } })</code></pre>

### 7️⃣ $in (In)
**Descrição:** Encontra documentos onde o valor do campo **corresponde a qualquer valor** em um array especificado.
<pre><code>// Encontra documentos onde o status é "A" ou "D"
db.inventory.find({ "status": { $in: [ "A", "D" ] } })</code></pre>

### 8️⃣ $nin (Not In)
**Descrição:** Encontra documentos onde o valor do campo **não corresponde a nenhum valor** em um array especificado.
<pre><code>// Encontra documentos onde o status não é "A" nem "D"
db.inventory.find({ "status": { $nin: [ "A", "D" ] } })</code></pre>

---

## 🔹 Operadores Lógicos

### 1️⃣ $and (E)
**Descrição:** Retorna documentos que satisfazem **todas** as condições em um array de expressões.
<pre><code>db.inventory.find({
    $and: [
        { "price": { $ne: 1.99 } },
        { "qty": { $lt: 20 } }
    ]
})
</code></pre>
> 💡 **AND Implícito:** Para a maioria das consultas, você pode especificar um `AND` implicitamente separando as condições com vírgula no documento de filtro: `db.inventory.find({ "price": { $ne: 1.99 }, "qty": { $lt: 20 } })`

### 2️⃣ $or (OU)
**Descrição:** Retorna documentos que satisfazem **pelo menos uma** das condições em um array de expressões.
<pre><code>db.inventory.find({
    $or: [
        { "qty": { $lt: 20 } },
        { "price": 10 }
    ]
})
</code></pre>

### 3️⃣ $nor (NÃO OU)
**Descrição:** Retorna documentos que **falham em todas** as condições em um array de expressões.
<pre><code>db.inventory.find({
    $nor: [
        { "price": 1.99 },
        { "qty": { $lt: 20 } }
    ]
})
</code></pre>

### 4️⃣ $not (NÃO)
**Descrição:** Inverte o efeito de uma expressão de consulta, retornando documentos que **não correspondem** à condição.
<pre><code>// Encontra documentos onde a quantidade NÃO é maior que 50
db.inventory.find({ "qty": { $not: { $gt: 50 } } })
</code></pre>