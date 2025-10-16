# 🗑️ Excluindo Bancos de Dados e Coleções

[MATERIAL DE APOIO: db.collection.drop()](https://www.mongodb.com/docs/manual/reference/method/db.collection.drop/)
[MATERIAL DE APOIO: db.dropDatabase()](https://www.mongodb.com/docs/manual/reference/method/db.dropDatabase/)

---

Este guia mostra como excluir coleções e bancos de dados inteiros, tanto pela interface gráfica (Compass) quanto pela linha de comando (Shell).

## 🔹 Método 1: Usando o MongoDB Compass (Interface Gráfica)

### 1️⃣ Excluindo uma Coleção
**Descrição:** Remove uma coleção específica de dentro de um banco de dados.

**Passos:**
1.  No painel à esquerda, expanda o banco de dados para ver suas coleções.
2.  Passe o mouse sobre a coleção que deseja remover e clique no **ícone de lixeira (🗑️)** que aparece.
3.  Uma janela de confirmação surgirá. Digite o **nome da coleção** para confirmar.
4.  Clique no botão **"Drop Collection"**.

### 2️⃣ Excluindo um Banco de Dados
**Descrição:** Remove um banco de dados inteiro, incluindo todas as suas coleções.

**Passos:**
1.  No painel à esquerda, passe o mouse sobre o banco de dados que deseja remover e clique no **ícone de lixeira (🗑️)**.
2.  Uma janela de confirmação surgirá. Digite o **nome do banco de dados** para confirmar.
3.  Clique no botão **"Drop Database"**.

---

## 🔹 Método 2: Usando o Mongo Shell (Linha de Comando)

### 1️⃣ Excluindo uma Coleção
**Descrição:** Remove uma coleção do banco de dados que você está usando atualmente.

**Passos:**
1.  Primeiro, certifique-se de que está usando o banco de dados correto com o comando `use <nome_do_banco>`.
2.  Para ver as coleções no banco atual, use `show collections`.
3.  Execute o comando `drop()` na coleção desejada. O comando retornará `true` se for bem-sucedido.
    <pre><code>db.nome_da_colecao.drop()</code></pre>
> 💡 Se o nome da coleção contiver espaços ou caracteres especiais, use colchetes e aspas: `db["nome da colecao"].drop()`

### 2️⃣ Excluindo um Banco de Dados
**Descrição:** Remove o banco de dados que você está usando atualmente.

**Passos:**
1.  **Importante:** Entre no banco de dados que você deseja excluir.
    <pre><code>use nome_do_banco_a_ser_excluido</code></pre>
2.  Execute o comando `dropDatabase()`.
    <pre><code>db.dropDatabase()</code></pre>
3.  O shell retornará uma mensagem de sucesso, confirmando a exclusão.

> ⚠️ **Cuidado:** Excluir um banco de dados é uma ação irreversível e remove **todos** os dados e coleções contidos nele. Se um banco de dados ficar sem nenhuma coleção, o MongoDB o remove automaticamente.