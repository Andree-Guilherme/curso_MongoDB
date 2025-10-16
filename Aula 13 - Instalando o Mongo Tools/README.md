# 🛠️ Instalando o MongoDB Database Tools

[MATERIAL DE APOIO: MongoDB Database Tools](https://www.mongodb.com/try/download/database-tools)

---

Este guia explica como instalar as Ferramentas de Banco de Dados do MongoDB (que incluem `mongodump`, `mongorestore`, etc.) em um ambiente Windows.

> 💡 **O que são as Database Tools?** São um conjunto de utilitários de linha de comando para trabalhar com o MongoDB, essenciais para backups (`mongodump`), restaurações (`mongorestore`), importação/exportação (`mongoimport`/`mongoexport`), e mais.

## 🔽 Passo 1: Download do Pacote

**Ações:**
1.  Acesse a página de download do [MongoDB Database Tools](https://www.mongodb.com/try/download/database-tools).
2.  Selecione a **versão** (geralmente a mais recente), a **plataforma** (Windows) e o **pacote** (Package) como **ZIP**.
3.  Clique em **Download**.

---

## 📂 Passo 2: Extração dos Arquivos

**Descrição:** Os arquivos baixados precisam ser colocados em um local acessível. Uma boa prática é colocá-los junto à instalação principal do MongoDB.

**Ações:**
1.  Navegue até a pasta de instalação do MongoDB Server. O caminho padrão é `C:\ Program Files\MongoDB\Server\<sua_versao>\`.
2.  Dentro da pasta da sua versão, crie um novo diretório chamado `tools`.
3.  Extraia o conteúdo do arquivo `.zip` que você baixou.
4.  Copie todos os arquivos da pasta `bin` (de dentro do ZIP) para a nova pasta `C:\ Program Files\MongoDB\Server\<sua_versao>\tools`.

---

## ⚙️ Passo 3: Configuração das Variáveis de Ambiente

**Descrição:** Adicionar a nova pasta `tools` ao "Path" do Windows permite que você execute os comandos (`mongodump`, etc.) de qualquer lugar no terminal.

**Ações:**
1.  Pressione **Win + R**, digite `sysdm.cpl` e pressione **Enter**.
2.  Vá para a aba **"Avançado"** e clique em **"Variáveis de Ambiente"**.
3.  Na seção **"Variáveis do sistema"**, encontre e selecione a variável **"Path"** e clique em **"Editar"**.
4.  Clique em **"Novo"** e adicione o caminho completo para a sua pasta `tools`.
    *   **Exemplo:** `C:\ Program Files\MongoDB\Server\6.0\tools`
5.  Clique em **"OK"** em todas as janelas para salvar as alterações.

---

## ✅ Passo 4: Verificação da Instalação

**Descrição:** Verifique se o Windows reconhece os novos comandos.

**Ações:**
1.  **Reinicie o computador** ou, no mínimo, feche e reabra qualquer terminal (CMD, PowerShell) que estiver aberto.
2.  Abra um novo terminal e digite o seguinte comando:
    <pre><code>mongodump --version</code></pre>
3.  Se a instalação foi bem-sucedida, você verá a versão do `mongodump` e outras informações.
