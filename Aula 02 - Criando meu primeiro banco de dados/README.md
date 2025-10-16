# 🗄️ Criando Meu Primeiro Banco de Dados

[MATERIAL DE APOIO: Comando 'use'](https://www.mongodb.com/docs/manual/reference/command/use/)

---

Este guia mostra duas maneiras de criar um banco de dados no MongoDB: através da interface gráfica (Compass) ou pela linha de comando (Mongo Shell).

## 🔹 Método 1: Usando o MongoDB Compass (Interface Gráfica)

### 1️⃣ Conectar ao Servidor
**Descrição:** Primeiro, estabeleça a conexão com o seu servidor MongoDB.

**Passos:**
1.  Na tela inicial do Compass, clique em **"Add new connection"**.
2.  Mantenha a URI padrão para conexão local:
    <pre><code>mongodb://localhost:27017/</code></pre>
3.  Clique em **"Save & Connect"** para salvar a conexão e acessar o servidor.

### 2️⃣ Criar o Banco de Dados e a Primeira Coleção
**Descrição:** Crie o novo banco de dados e, obrigatoriamente, sua primeira coleção.

**Passos:**
1.  No painel à esquerda, clique no botão **"Create Database"**.
2.  Na janela que surgir, preencha os dois campos:
    *   **Database Name:** O nome do seu novo banco (ex: `loja`).
    *   **Collection Name:** O nome da primeira coleção (ex: `produtos`).
3.  Clique em **"Create Database"** para finalizar.

> 💡 **Importante:** No MongoDB, um banco de dados só é fisicamente criado após a inserção do primeiro documento ou a criação da primeira coleção. Por isso, o Compass solicita ambos os nomes.

> ℹ️ **Bancos Padrão:** Ao se conectar, você verá 3 bancos de dados já existentes: `admin` (credenciais e configurações globais), `config` (usado para sharding) e `local` (dados específicos do nó, não replicado).

---

## 🔹 Método 2: Usando o Mongo Shell (Linha de Comando)

### 1️⃣ Iniciar e Conectar
**Descrição:** Abra o terminal e inicie o Mongo Shell.

<pre><code>mongosh</code></pre>

### 2️⃣ Listar Bancos Existentes (Opcional)
**Descrição:** Use o comando `show databases` para ver todos os bancos de dados no servidor.

<pre><code>show databases</code></pre>

### 3️⃣ Criar o Novo Banco de Dados
**Descrição:** Para criar um banco via shell, você primeiro seleciona o nome do banco com `use` e depois cria uma coleção dentro dele.

**Passos:**
1.  Digite `use <nome_do_banco>` para mudar para o seu novo banco de dados. Ele ainda não será criado.
    <pre><code>use loja</code></pre>
2.  Crie a primeira coleção para que o banco seja salvo.
    <pre><code>db.createCollection("produtos")</code></pre>
3.  O shell retornará `{ "ok" : 1 }`, confirmando que a operação foi bem-sucedida.

> ⚠️ **Lembre-se:** O comando `use` também serve para **alternar** entre bancos de dados que já existem. O MongoDB é **case sensitive**, então `loja` e `Loja` são considerados bancos diferentes.