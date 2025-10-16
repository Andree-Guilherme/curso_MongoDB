# 🔎 Consultando Dados com MongoDB Compass

[MATERIAL DE APOIO: Filtrando Documentos no Compass](https://www.mongodb.com/docs/compass/current/query/filter/)

---

Este guia explica como usar a barra de consulta e as opções de filtro no MongoDB Compass para encontrar e organizar seus dados.

## 🔹 A Barra de Consulta (Query Bar)

A barra de consulta, localizada no topo da visualização de uma coleção, é a principal ferramenta para buscar documentos. Ela é composta por várias partes.

### 1️⃣ Filter (Filtro)
**Descrição:** É o campo principal onde você define as condições para encontrar documentos.

**Uso:**
*   Para encontrar todos os documentos, deixe o filtro vazio: `{}`.
*   Para encontrar documentos que correspondem a uma condição, especifique um campo e um valor.

**Exemplo:** Para achar todos os usuários com o nome "André":
<pre><code>{ "nome": "André" }</code></pre>

> 💡 Se a sintaxe do filtro estiver incorreta, o botão **"Find"** ficará desabilitado.

### 2️⃣ Project (Projeção)
**Descrição:** Define quais campos (colunas) devem ser incluídos ou excluídos dos resultados.

**Uso:**
*   `1`: Inclui o campo no resultado.
*   `0`: Exclui o campo do resultado.

**Exemplo:** Para mostrar apenas o campo `nome` e `email`, e excluir o `_id`:
<pre><code>{ "_id": 0, "nome": 1, "email": 1 }</code></pre>

### 3️⃣ Sort (Ordenação)
**Descrição:** Ordena os documentos retornados com base em um ou mais campos.

**Uso:**
*   `1`: Ordena em ordem ascendente (A-Z, 0-9).
*   `-1`: Ordena em ordem descendente (Z-A, 9-0).

**Exemplo:** Para ordenar os usuários por nome, em ordem alfabética:
<pre><code>{ "nome": 1 }</code></pre>

### 4️⃣ Outras Opções (Options)
Clicando em **"Options"**, você tem acesso a mais filtros:

*   **Collation:** Permite buscas que ignoram maiúsculas/minúsculas ou acentos.
    *   **Exemplo:** `{ "locale": "pt", "strength": 2 }` (Busca em português, ignorando acentos e capitalização).
*   **Skip:** Pula um número de documentos no resultado. Útil para paginação.
    *   **Exemplo:** `{ "skip": 10 }` (Pula os 10 primeiros resultados).
*   **Limit:** Limita o número de documentos retornados pela busca.
    *   **Exemplo:** `{ "limit": 5 }` (Mostra no máximo 5 documentos).
*   **Max Time MS:** Define um tempo máximo (em milissegundos) para a execução da consulta.

---

> 💡 **Busca Inteligente:** O campo **"Tell us what to find"** permite que você escreva o que quer em linguagem natural, e o Compass tentará converter sua frase em um filtro JSON válido.