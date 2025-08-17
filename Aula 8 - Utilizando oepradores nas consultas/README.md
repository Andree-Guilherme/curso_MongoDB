# 📌 MongoDB Query Operators Step-by-Step

[MATERIAL DE APOIO](https://www.mongodb.com/pt-br/docs/manual/reference/operator/query/)

---

## 🔹 Comparação

### 1️⃣ $eq – Igualdade ( = )

<pre><code>db.&lt;collection&gt;.find({
    "&lt;key&gt;": {
        $eq: &lt;value&gt;
    }
});</code></pre>

**Objetivo:** Encontrar documentos em que o valor de um campo seja exatamente igual ao valor especificado.

---

### 2️⃣ $gt – Maior que ( > )

<pre><code>db.&lt;collection&gt;.find({
    "&lt;key&gt;": {
        $gt: &lt;value&gt;
    }
});</code></pre>

**Objetivo:** Encontra documentos em que o valor do campo seja maior que o valor especificado.

---

### 3️⃣ $gte – Maior ou igual a ( ≥ )

<pre><code>db.&lt;collection&gt;.find({
    "&lt;key&gt;": {
        $gte: &lt;value&gt;
    }
});</code></pre>

**Objetivo:** Encontra documentos em que o valor do campo seja maior ou igual ao valor especificado.

---

### 4️⃣ $in – Contido em ( ∈ )

<pre><code>db.&lt;collection&gt;.find({
    "&lt;key&gt;": {
        $in: [&lt;value1&gt;, &lt;value2&gt;, ...]
    }
});</code></pre>

**Objetivo:** Encontra documentos em que o valor do campo esteja dentro de uma lista de valores especificada.

---

### 5️⃣ $lt – Menor que ( < )

<pre><code>db.&lt;collection&gt;.find({
    "&lt;key&gt;": {
        $lt: &lt;value&gt;
    }
});</code></pre>

**Objetivo:** Encontra documentos em que o valor do campo seja menor que o valor especificado.

---

### 6️⃣ $lte – Menor ou igual a ( ≤ )

<pre><code>db.&lt;collection&gt;.find({
    "&lt;key&gt;": {
        $lte: &lt;value&gt;
    }
});</code></pre>

**Objetivo:** Encontra documentos em que o valor do campo seja menor ou igual ao valor especificado.

---

### 7️⃣ $ne – Diferente de ( ≠ )

<pre><code>db.&lt;collection&gt;.find({
    "&lt;key&gt;": {
        $ne: &lt;value&gt;
    }
});</code></pre>

**Objetivo:** Encontra documentos em que o valor do campo seja diferente do valor especificado.

---

### 8️⃣ $nin – Não contido em ( ∉ )

<pre><code>db.&lt;collection&gt;.find({
    "&lt;key&gt;": {
        $nin: [&lt;value1&gt;, &lt;value2&gt;, ...]
    }
});</code></pre>

**Objetivo:** Encontra documentos em que o valor do campo não esteja dentro de uma lista de valores especificada.

---

## 🔹 Lógica

### 1️⃣ $and – E lógico ( ∧ )

<pre><code>db.&lt;collection&gt;.find({
    $and: [
        { "&lt;key1&gt;": &lt;value1&gt; },
        { "&lt;key2&gt;": &lt;value2&gt; }
    ]
});
</code></pre>

**Objetivo:** Retorna documentos que satisfaçam **todas as condições** especificadas.

---

### 2️⃣ $not – Negação lógica ( ¬ )

<pre><code>db.&lt;collection&gt;.find({
    "&lt;key&gt;": {
        $not: { &lt;comparison&gt;: &lt;value&gt; }
    }
});
</code></pre>

**Objetivo:** Retorna documentos que **não correspondam** ao predicado especificado.

---

### 3️⃣ $nor – NOR lógico ( ⊽ )

<pre><code>db.&lt;collection&gt;.find({
    $nor: [
        { "&lt;key1&gt;": &lt;value1&gt; },
        { "&lt;key2&gt;": &lt;value2&gt; }
    ]
});
</code></pre>

**Objetivo:** Retorna documentos que **não correspondam a nenhuma** das condições fornecidas.

---

### 4️⃣ $or – OU lógico ( ∨ )

<pre><code>db.&lt;collection&gt;.find({
    $or: [
        { "&lt;key1&gt;": &lt;value1&gt; },
        { "&lt;key2&gt;": &lt;value2&gt; }
    ]
});
</code></pre>

**Objetivo:** Retorna documentos que satisfaçam **pelo menos uma das condições**.
