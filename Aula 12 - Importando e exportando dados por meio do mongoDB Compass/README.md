# ✏️Importando e exportando dados por meio do mongoDB Compass

## 📤 Exportando Dados de uma Coleção (Backup)

## 🔹 Exportação passo a passo

1.  Abra a **Collection** que deseja exportar.
2.  Clique no botão **EXPORT DATA**.
3.  Será exibida uma tela perguntando o **formato do arquivo** para exportação:
    *   **JSON**
    *   **CSV**
4.  Escolha o formato desejado (recomenda-se **JSON** para backup completo).
5.  Selecione se deseja exportar:
    *   **Todos os documentos da coleção**
    *   **Apenas os resultados do filtro atual**
6.  Clique em **Export** e escolha onde salvar o arquivo no seu computador.

✅ O arquivo gerado servirá como **backup** e poderá ser importado novamente quando necessário.

---

## 📥 Importando Dados Exportados (Backup)

Quando precisar restaurar ou reaproveitar esses dados, siga o processo:

## 🔹 Import JSON ou CSV

1.  Dentro da **Collection**, clique em **ADD DATA** > **Import JSON or CSV file**.
2.  Será aberta a tela de importação, como na imagem mostrada:

---

### ⚙️ Tela de Importação

*   **Import file**: selecione o arquivo `.json` ou `.csv` exportado anteriormente.
*   **Options**:
    *   _Select delimiter_: escolha o delimitador (para CSV, normalmente vírgula).
    *   _Ignore empty strings_: ignora campos vazios.
    *   _Stop on errors_: interrompe se ocorrer algum erro.

---

### 📄 Specify Fields and Types

*   O Mongo detecta automaticamente os campos e tipos de dados.
*   Você pode ajustar o tipo de dado de cada campo:
    *   `ObjectId`
    *   `String`
    *   `Int32`, `Double`, `Date`, etc.
*   A tabela exibirá uma prévia dos documentos que serão importados.
*   Se necessário, marque ou desmarque os campos que deseja importar.