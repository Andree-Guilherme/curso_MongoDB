# ✏️ Inserindo Dados em uma Coleção

---

## 🔹 Inserção passo a passo

1. Para inserir dados dentro da collection via **interface gráfica**, clique em **ADD DATA**.
2. Será perguntado se deseja:  
   - **Import JSON or CSV file**  
   - **Insert document**
3. Abrirá uma tela para inserir o documento.
4. Existem duas formas de inserir os dados nessa tela:  
   - **VIEW JSON** – insere o documento no formato JSON.  
   - **VIEW Simplificada (linha a linha)** – insere campo a campo.
5. Após inserir os dados em qualquer uma das views, o Mongo gera automaticamente um **ID** para o documento.
6. Por fim, clique em **Insert** para concluir a inserção.

---

### 📄 VIEW JSON

- Insira o documento no formato JSON, que é o padrão.
- Pode usar o modelo já preenchido pelo Mongo ou apagar as informações para inserir um novo JSON.
- O Mongo gera automaticamente o campo de **ID** (`_id`), então não é necessário declará-lo manualmente.
- A sintaxe deve seguir o padrão JSON válido para inserção de dados.

---

### 📝 VIEW Simplificada (linha a linha)

- A inserção é feita campo a campo, como se fosse uma tabela.
- Adicione os valores e selecione o tipo de dado para cada campo.
- Para adicionar um novo campo, clique no símbolo de **+**.
- Para excluir um campo, clique no ícone de **lixeira**.