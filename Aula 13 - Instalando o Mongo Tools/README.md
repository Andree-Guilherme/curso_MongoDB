# 🛠️ Como Instalar o MongoDB Database Tools (via ZIP)

## 🔽 Download MongoDB Tools

1.  Acesse o site [MongoDB Tools](https://www.mongodb.com/try/download/database-tools)
2.  Selecione os seguintes campos:
    *   **Version**
    *   **Platform**
    *   **Package** → _ZIP_
3.  Clique em **Download**

---

## 📂 Criando a Pasta `tools`

1.  Acesse o diretório onde o **MongoDB** foi instalado (exemplo: `C:\Program Files\MongoDB\Server\X.X\`)
2.  Crie uma nova pasta chamada **tools**
3.  Extraia os arquivos baixados do **ZIP**
4.  Copie todo o conteúdo extraído para dentro da pasta **tools** criada

---

## ⚙️ Configurando Variáveis de Ambiente

1.  Pressione as teclas **Win + R**
2.  Digite `sysdm.cpl` e pressione **Enter**
3.  Na janela aberta, vá até a aba **Avançado**
4.  Clique em **Variáveis de Ambiente**
5.  Em **Variáveis do sistema**, localize a variável **Path**
6.  Clique em **Editar**
7.  Clique em **Novo** e cole o caminho da pasta **tools** criada:
    *   Exemplo: `C:\Program Files\MongoDB\tools`
8.  Clique em **OK** em todas as janelas para salvar

---

## ✅ Testando a Instalação

1.  Reinicie o PC
2.  Abra o **Prompt de Comando** (CMD) ou **PowerShell**
3.  Digite: `mongodump --version`