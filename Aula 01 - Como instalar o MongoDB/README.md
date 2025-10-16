# 📥 Como Instalar o MongoDB

[MATERIAL DE APOIO: MongoDB Community Server](https://www.mongodb.com/try/download/community)
[MATERIAL DE APOIO: MongoDB Shell (mongosh)](https://www.mongodb.com/try/download/shell)

---

## 🔽 Passo 1: Download dos Pacotes

### 1️⃣ MongoDB Community Server
**Descrição:** Baixe o instalador principal do MongoDB, que inclui o banco de dados e a interface gráfica Compass.

**Ações:**
1.  Acesse o site do [MongoDB Community Server](https://www.mongodb.com/try/download/community).
2.  Selecione a **versão**, **plataforma** (geralmente Windows) e **pacote** (MSI).
3.  Clique em **Download**.

### 2️⃣ MongoDB Shell (mongosh)
**Descrição:** Baixe o shell (linha de comando) para interagir com o banco de dados.

**Ações:**
1.  Acesse o site do [MongoDB Shell](https://www.mongodb.com/try/download/shell).
2.  Escolha as mesmas opções de **versão** e **plataforma** do passo anterior.
3.  Clique em **Download**.

> ⚠️ **Atenção:** É importante que a versão do `mongosh` seja compatível com a versão do MongoDB Server para evitar problemas.

---

## ⚙️ Passo 2: Instalação e Configuração

### 1️⃣ Instalando o MongoDB Server
**Descrição:** Siga o assistente de instalação para configurar o MongoDB como um serviço no Windows.

**Passos:**
1.  Execute o instalador `.msi` do **MongoDB Server** como administrador.
2.  Clique em **Next** e **aceite os termos** da licença.
3.  Escolha o tipo de instalação **"Complete"** (Completa).
4.  Na tela de configuração de serviço, mantenha as opções padrão marcadas:
    *   `Install MongoD as a Service` (Instalar como serviço).
    *   `Run service as Network Service user`.
5.  Anote ou altere os diretórios de **Dados (Data)** e **Logs**.
6.  Clique em **Next**.
7.  **Marque a opção** para `Install MongoDB Compass` (a interface gráfica).
8.  Clique em **Next**, depois em **Install** e aguarde a conclusão.
9.  Finalize clicando em **Finish**.

### 2️⃣ Instalando o Mongo Shell
**Descrição:** Instale a ferramenta de linha de comando.

**Passos:**
1.  Execute o instalador `.msi` do **Mongo Shell** como administrador.
2.  Na tela de seleção, **desmarque** a opção `Install just for you` para que o `mongosh` fique disponível para todos os usuários do sistema e seja adicionado ao PATH do Windows.
3.  Clique em **Install** e aguarde.
4.  Finalize clicando em **Finish**.

> ✅ **Recomendação:** Após concluir as duas instalações, reinicie o computador para garantir que todas as variáveis de ambiente sejam carregadas corretamente.