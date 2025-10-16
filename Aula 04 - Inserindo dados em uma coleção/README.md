# ✏️ Inserindo Dados em uma Coleção (via Compass)

[MATERIAL DE APOIO: Inserindo Documentos](https://www.mongodb.com/docs/manual/core/document/#insert-documents)

---

Este guia foca em como inserir novos documentos em uma coleção utilizando a interface gráfica do MongoDB Compass.

## 🔹 Inserindo Documentos com o MongoDB Compass

Dentro de uma coleção, clique no botão **"ADD DATA"**. Você terá duas opções principais:

1.  **Import JSON or CSV file:** Permite carregar um arquivo com múltiplos documentos de uma vez.
2.  **Insert Document:** Abre uma interface para adicionar um único documento manualmente.

Este guia detalha a segunda opção, **"Insert Document"**.

---

### 1️⃣ Inserindo um Único Documento

Ao escolher **"Insert Document"**, uma janela aparecerá com duas abas para a inserção dos dados:

#### Modo 1: Visualização em Lista (Padrão)
**Descrição:** Um formulário simples onde você adiciona campos e valores linha a linha.

**Passos:**
1.  Por padrão, um campo `_id` já vem preenchido. Você pode mantê-lo ou removê-lo para que o MongoDB gere um automaticamente.
2.  Para adicionar um novo campo, clique no **ícone de mais (+)**.
3.  Digite o **nome do campo** (ex: `nome`), o **tipo de dado** (ex: `String`) e o **valor** (ex: `"Produto A"`).
4.  Repita para todos os campos que desejar.
5.  Clique em **"Insert"** para salvar o documento.

#### Modo 2: Visualização em JSON
**Descrição:** Permite colar ou escrever o documento diretamente no formato JSON.

**Passos:**
1.  Clique na aba **`{ }`** para mudar para a visualização em JSON.
2.  Você verá um template com o `_id`. Você pode apagar tudo e colar seu próprio JSON ou apenas editar os campos.
3.  Escreva seu documento seguindo a sintaxe JSON.
    <pre><code>{
  "nome": "Produto B",
  "preco": 29.99,
  "em_estoque": true
}
</code></pre>
4.  Clique em **"Insert"** para salvar o documento.

> 💡 **Geração Automática de ID:** Se você não especificar um campo `_id` ao inserir um documento, o MongoDB criará automaticamente um `ObjectId` único para ele. Esta é a prática mais comum.
