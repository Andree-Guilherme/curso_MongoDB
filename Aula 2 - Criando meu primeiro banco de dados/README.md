# 🗄️ Criando Meu Primeiro Banco de Dados

---

## 🔌 Conectando ao banco

1. Para criar um banco de dados, primeiro devemos nos conectar a ele clicando em **Add new connection**.
2. Depois irá aparecer a tela de **New Connection** onde definiremos a **URI (String de Conexão)**.
3. Deixe a URI padrão:  
   <pre><code>mongodb://localhost:27017/</code></pre>
4. Salvar as informações:
   - **Save:** Salva as configurações ou dados atuais.
   - **Connect:** Sempre será necessário clicar para conectar, mesmo após salvar.
   - **Save & Connect:** Permite reconexão automática sem precisar clicar manualmente toda vez.
5. Feito isso, já estamos conectados ao servidor local.

---

## 🏗️ Criando o banco de dados

1. Ao se conectar, por padrão já existem 3 bancos de dados:
   - **admin** – Banco administrativo que armazena credenciais, roles e configurações de nível global.
   - **config** – Usado pelo sharding para guardar metadados e informações de configuração dos shards.
   - **local** – Guarda dados locais do nó, como informações de replicação; não é replicado entre servidores.
2. Para criar um novo banco de dados, clique no botão **Create Database**.
3. Será aberta uma tela solicitando:
   - **Database Name**
   - **Collection Name**  

   > Por padrão, sempre deve ser criada **uma collection junto com o banco**.  
   > *Em analogia a um banco relacional, uma collection seria uma tabela, mas não é exatamente a mesma coisa.*
4. Clique em **Create Database** para finalizar.

---

## 💻 Criando o banco via Shell

1. Abra o `CMD` e digite:  
   <pre><code>mongosh</code></pre>  
   para se **conectar ao banco de dados**.  

   **Importante:** Ao conectar, o shell mostra:
   - O caminho em que está se conectando
   - A versão do MongoDB
   - A versão do shell
2. Para **exibir os bancos de dados existentes**, use:  
   <pre><code>show databases</code></pre>
3. Para **criar um novo banco de dados**, execute:
   1. <pre><code>use {nome_do_banco}</code></pre>
   2. <pre><code>db.createCollection("{nome_da_collection}")</code></pre>  

   > O comando `use` muda o banco atual mesmo que ainda não exista.  
   > Sempre devemos criar uma **collection junto com o banco** para que ele seja criado de fato.
4. Será retornada uma mensagem com `ok`.
5. Banco de dados criado com sucesso.

> ⚠️ O comando `use` também serve para **alternar entre bancos já existentes**.  
> 🔹 O MongoDB é **case sensitive**, portanto digite os nomes de bancos e comandos corretamente.
