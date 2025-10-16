# 💾 Usando mongodump e mongorestore

[MATERIAL DE APOIO: mongodump](https://www.mongodb.com/docs/database-tools/mongodump/)
[MATERIAL DE APOIO: mongorestore](https://www.mongodb.com/docs/database-tools/mongorestore/)

---

`mongodump` e `mongorestore` são ferramentas de linha de comando essenciais para criar backups (dumps) e restaurar dados no MongoDB.

> 💡 **BSON vs JSON:** `mongodump` exporta dados em formato **BSON** (Binary JSON), que é uma representação binária de alta performance, ideal para backups. É diferente do formato JSON de texto simples.

## 📤 Exportando Dados com mongodump (Backup)

### 1️⃣ Exportar um banco de dados inteiro
**Descrição:** Cria um backup completo de um banco de dados específico.
<pre><code>mongodump --db &lt;nome_do_banco&gt; --out &lt;caminho_da_pasta&gt;
</code></pre>

### 2️⃣ Exportar apenas uma coleção
**Descrição:** Cria um backup de uma única coleção.
<pre><code>mongodump --db &lt;nome_do_banco&gt; --collection &lt;nome_da_colecao&gt; --out &lt;caminho_da_pasta&gt;
</code></pre>

### 3️⃣ Exportar um banco, exceto uma coleção
**Descrição:** Útil para excluir coleções grandes ou temporárias do backup.
<pre><code>mongodump --db &lt;nome_do_banco&gt; --excludeCollection &lt;nome_da_colecao&gt; --out &lt;caminho_da_pasta&gt;
</code></pre>

### 4️⃣ Exportar usando uma URI de conexão
**Descrição:** Permite conectar a um servidor remoto (como o Atlas) ou local usando uma string de conexão.
<pre><code># Para um banco de dados inteiro
mongodump --uri "mongodb://user:pass@host:port/db_name" --out &lt;caminho_da_pasta&gt;

# Para uma única coleção
mongodump --uri "mongodb://user:pass@host:port/db_name" --collection &lt;nome_da_colecao&gt; --out &lt;caminho_da_pasta&gt;
</code></pre>

---

## 📥 Importando Dados com mongorestore (Restauração)

### 1️⃣ Restaurar um banco de dados
**Descrição:** Restaura um backup completo para um banco de dados. Se o banco não existir, ele será criado.
<pre><code># O último argumento é a pasta que contém o backup
mongorestore --db &lt;nome_do_banco&gt; &lt;caminho_da_pasta_de_backup&gt;
</code></pre>

### 2️⃣ Restaurar apenas uma coleção
**Descrição:** Restaura um único arquivo de coleção (BSON) para dentro de um banco.
<pre><code># O último argumento é o caminho para o arquivo .bson da coleção
mongorestore --db &lt;nome_do_banco&gt; --collection &lt;nome_da_colecao&gt; &lt;caminho_para_o_arquivo.bson&gt;
</code></pre>

### 3️⃣ Restaurar para um servidor remoto (via URI)
**Descrição:** Usa uma string de conexão para restaurar dados em um servidor remoto, como o MongoDB Atlas.
<pre><code>mongorestore --uri "mongodb://user:pass@host:port/" --db &lt;nome_do_banco&gt; &lt;caminho_da_pasta_de_backup&gt;
</code></pre>

---

> ⚠️ **Sobrescrever Dados:** Por padrão, o `mongorestore` **não apaga** os dados existentes na coleção de destino. Se você deseja limpar a coleção antes de inserir os novos dados (substituir em vez de adicionar), use a flag `--drop`.
> <pre><code>mongorestore --drop --db &lt;nome_do_banco&gt; &lt;caminho_da_pasta_de_backup&gt;</code></pre>