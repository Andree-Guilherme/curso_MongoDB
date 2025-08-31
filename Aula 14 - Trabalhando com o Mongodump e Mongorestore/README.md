# 💾 Trabalhando com Mongodump e Mongorestore

---

## 1️⃣ Exportando dados com **mongodump**

### Exportar um banco de dados inteiro
<pre><code>mongodump --db &lt;database&gt; --out &lt;directory_path&gt;
</code></pre>

**Passos:**
1. Substitua `<database>` pelo nome do banco.
2. Substitua `<directory_path>` pelo caminho da pasta onde deseja salvar o backup.
3. Será criada uma pasta com o nome do banco dentro do diretório informado.

---

### Exportar apenas uma collection
<pre><code>mongodump --db &lt;database&gt; --collection &lt;collection&gt; --out &lt;directory_path&gt;
</code></pre>

**Passos:**
1. Use quando quiser salvar somente uma collection específica.
2. A exportação será gravada no diretório informado.

---

### Exportar todas collections exceto uma
<pre><code>mongodump --db &lt;database&gt; --excludeCollection &lt;collection&gt; --out &lt;directory_path&gt;
</code></pre>

**Passos:**
1. Substitua `<collection>` pela que não deve ser incluída no backup.
2. Todas as outras collections do banco serão exportadas normalmente.

---

### Exportar usando URI de conexão (apenas uma collection)
<pre><code>mongodump --uri "&lt;connection_string&gt;" --collection &lt;collection&gt; --out &lt;directory_path&gt;
</code></pre>

**Passos:**
1. Cole a string de conexão do cluster Atlas ou servidor local em `<connection_string>`.
2. Informe a collection que deseja exportar.

---

### Exportar usando URI de conexão (banco inteiro)
<pre><code>mongodump --uri "&lt;connection_string&gt;" --out &lt;directory_path&gt;
</code></pre>

**Passos:**
1. Usa a conexão para exportar todos os bancos (ou conforme permissões do usuário).
2. O backup é gravado no diretório informado.

---

## 2️⃣ Importando dados com **mongorestore**

### Restaurar um banco a partir de backup
<pre><code>mongorestore --db &lt;database&gt; &lt;directory_path&gt;
</code></pre>

**Passos:**
1. Substitua `<database>` pelo nome do banco que receberá os dados.
2. Informe o caminho do backup feito pelo `mongodump`.

---

### Restaurar para Atlas ou servidor via URI
<pre><code>mongorestore --uri "&lt;connection_string&gt;" --db &lt;database&gt; c:\curso\GameControll
</code></pre>

**Passos:**
1. Use a URI do cluster (`<connection_string>`).
2. Escolha o banco (`<database>`).
3. Informe o caminho local do backup.

---

### Restaurar apenas uma collection
<pre><code>mongorestore --uri "&lt;connection_string&gt;" --collection &lt;collection&gt; --db &lt;database&gt; &lt;file_path&gt;
</code></pre>

**Passos:**
1. Indique a URI de conexão.
2. Selecione o banco (`<database>`) e a collection (`<collection>`).
3. Passe o caminho direto do arquivo BSON da collection (`<file_path>`).

---

> ⚠️ **Atenção:** por padrão, o `mongorestore` insere os dados sem apagar os existentes. Se quiser sobrescrever, adicione a flag `--drop`.
