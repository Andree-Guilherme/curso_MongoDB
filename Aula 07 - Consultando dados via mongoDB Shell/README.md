# 🔎 Consultando Dados via MongoDB Shell

[MATERIAL DE APOIO: Método find()](https://www.mongodb.com/docs/manual/reference/method/db.collection.find/)

---

## 🔹 Componentes da Consulta

Uma consulta com `find()` pode ser simples ou composta por vários métodos encadeados para refinar o resultado.

### 📄 Filtro (Filter)
O primeiro argumento do método `find()`. É um documento que define as condições de busca. Se omitido (`{}`), retorna todos os documentos.

### ✨ Projeção (Projection)
Define quais campos do documento serão incluídos (`1`) ou excluídos (`0`) do resultado final.

### 🔢 Ordenação (Sort)
Organiza os documentos retornados com base em um campo, em ordem ascendente (`1`) ou descendente (`-1`).

### 🌐 Collation
Define regras de um idioma específico para comparação de strings, como tratamento de acentos e maiúsculas.

### 💡 Dica de Índice (Hint)
Força o MongoDB a usar um índice específico para otimizar a performance da consulta.

---

## 🧩 Exemplos de Combinações

### 1️⃣ Apenas Filtro
**Descrição:** Retorna todos os documentos da coleção `users` que correspondem à condição `{ <"key">: <"value"> }`.
<pre><code>db.users.find({ <"key">: <"value"> });
</code></pre>

### 2️⃣ Filtro + Projeção
**Descrição:** Busca documentos e exclui o campo `<"key">` do resultado.
<pre><code>db.users.find(
  { <"key">: <"value"> }
).projection({ <"key">: 0 });
</code></pre>

### 3️⃣ Filtro + Ordenação
**Descrição:** Busca os documentos e os ordena de forma descendente (`-1`) pelo campo `<"key">`.
<pre><code>db.users.find({ <"key">: <"value"> })
        .sort({ <"key">: -1 });
</code></pre>

### 4️⃣ Filtro + Collation
**Descrição:** Aplica regras de comparação do idioma português (`locale: "pt"`) à busca.
<pre><code>db.users.find({ <"key">: <"value"> })
        .collation({ locale: "pt", strength: 2 });
</code></pre>

### 5️⃣ Filtro + Dica de Índice (Hint)
**Descrição:** Força a consulta a usar o índice `{ <"key">: 1 }` para otimizar a busca.
<pre><code>db.users.find({ <"key">: <"value"> })
        .hint({ <"key">: 1 });
</code></pre>

### 6️⃣ Filtro + Projeção + Ordenação
**Descrição:** Combina filtro, exclusão de dois campos e ordenação descendente.
<pre><code>db.users.find(
  { <"key">: <"value"> }
).projection({ <"key">: 0, <"key2">: 0 })
 .sort({ <"key">: -1 });
</code></pre>

### 7️⃣ Filtro + Ordenação + Collation
**Descrição:** Combina filtro, ordenação ascendente e regras de comparação de idioma.
<pre><code>db.users.find({ <"key">: <"value"> })
        .sort({ <"key">: 1 })
        .collation({ locale: "pt", strength: 1 });
</code></pre>

### 8️⃣ Filtro + Projeção + Collation
**Descrição:** Combina filtro, exclusão de um campo e regras de comparação de idioma.
<pre><code>db.users.find(
  { <"key">: <"value"> }
).projection({ <"key">: 0 })
 .collation({ locale: "pt", strength: 2 });
</code></pre>

### 9️⃣ Filtro + Dica de Índice + Ordenação
**Descrição:** Usa um operador (`$gte`), força um índice e ordena o resultado.
<pre><code>db.users.find({ <"key">: { $gte: <"value"> } })
        .hint({ <"key">: 1 })
        .sort({ <"key">: -1 });
</code></pre>

### 🔟 Filtro + Projeção + Ordenação + Collation + Dica de Índice
**Descrição:** Exemplo complexo que combina todos os parâmetros para refinar a busca.
<pre><code>db.users.find(
  { <"key">: <"value"> }
).projection({ <"key">: 0, <"key2">: 0 })
 .sort({ <"key">: 1 })
 .collation({ locale: "pt", strength: 2 })
 .hint({ <"key">: 1 });
</code></pre>

---

> 💡 Lembre-se: No MongoDB Compass, a opção `> Open Export to Language` converte sua busca para código em várias linguagens, facilitando a integração com sua aplicação!