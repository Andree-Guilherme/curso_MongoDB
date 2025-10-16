# 💾 Backup e Restauração com Import/Export (via Compass)

[MATERIAL DE APOIO: Importar e Exportar Dados no Compass](https://www.mongodb.com/docs/compass/current/import-export/)

---

Este guia mostra como usar as funções de exportação e importação do MongoDB Compass para criar e restaurar backups de suas coleções.

## 📤 Exportando uma Coleção (Criando um Backup)

**Descrição:** Salva os dados de uma coleção em um arquivo local (JSON ou CSV), que pode ser usado como backup.

**Passos:**
1.  Selecione a coleção da qual deseja fazer backup.
2.  Clique no menu **"Collection"** na parte superior e escolha **"Export Collection"**.
3.  Na janela de exportação, configure as opções de saída:
    *   **Export Full Collection:** Para fazer backup de **todos** os documentos.
    *   **Export Query Results:** Para fazer backup apenas do resultado de uma **consulta específica**.
4.  Escolha os campos a serem exportados em **"Select Fields"**.
5.  Selecione o formato de saída. Para um backup fiel, **JSON é recomendado**.
6.  Clique em **"EXPORT"** e salve o arquivo em um local seguro.

---

## 📥 Importando uma Coleção (Restaurando um Backup)

**Descrição:** Restaura os dados de um arquivo de backup (JSON ou CSV) para dentro de uma coleção.

**Passos:**
1.  Crie ou selecione a coleção de destino.
2.  Clique no botão **"ADD DATA"** e escolha **"Import JSON or CSV file"**.
3.  Selecione o arquivo de backup (`.json` ou `.csv`) do seu computador.
4.  **Configure os campos e tipos:**
    *   O Compass tentará detectar os tipos de dados automaticamente.
    *   Você pode corrigir o tipo de cada campo (ex: `String`, `Int32`, `ObjectId`) na tabela de pré-visualização.
    *   Marque ou desmarque os campos que deseja importar.
5.  **Configure as opções de importação:**
    *   `Stop on errors`: Interrompe o processo se um erro for encontrado.
    *   `Ignore empty strings`: Ignora campos com valores vazios.
6.  Clique em **"IMPORT"** para iniciar a restauração dos dados.

> 💡 **Dica:** Ao restaurar um backup, revisar os tipos de dados na etapa 4 é crucial para garantir a integridade dos dados, especialmente para campos como `ObjectId` e datas.
