# 📦 Importando e Exportando Dados (via Compass)

[MATERIAL DE APOIO: Importar Dados no Compass](https://www.mongodb.com/docs/compass/current/import-export/#import-data-into-a-collection)
[MATERIAL DE APOIO: Exportar Dados no Compass](https://www.mongodb.com/docs/compass/current/import-export/#export-data-from-a-collection)

---

Este guia detalha como usar o MongoDB Compass para importar e exportar dados de suas coleções.

## 📥 Importando Dados para uma Coleção

**Descrição:** Adiciona múltiplos documentos a uma coleção a partir de um arquivo JSON ou CSV.

**Passos:**
1.  No painel à esquerda, selecione o **banco de dados** e a **coleção** de destino.
2.  Com a coleção selecionada, clique no botão **"ADD DATA"** e escolha a opção **"Import JSON or CSV file"**.
3.  Na janela de importação, selecione o arquivo do seu computador.
4.  Configure as opções, se necessário (como o delimitador para CSV ou se a importação deve parar em caso de erro).
5.  Clique em **"IMPORT"** e aguarde a conclusão. Os dados do arquivo serão adicionados à sua coleção.

---

## 📤 Exportando Dados de uma Coleção

**Descrição:** Salva os documentos de uma coleção (ou de uma consulta) em um arquivo JSON ou CSV no seu computador.

**Passos:**
1.  Selecione a coleção que deseja exportar.
2.  Clique no menu **"Collection"** na parte superior e escolha **"Export Collection"**.
3.  Na janela de exportação, configure as opções:
    *   **Export Full Collection:** Para exportar todos os documentos.
    *   **Export Query Results:** Para exportar apenas o resultado de uma consulta específica (você deve inserir o filtro no campo `Filter`).
4.  Escolha os campos que deseja exportar clicando em **"Select Fields"**.
5.  Selecione o formato de saída (**JSON** ou **CSV**).
6.  Clique em **"EXPORT"**, escolha o local para salvar o arquivo e confirme.

> 💡 **Dica:** Exportar o resultado de uma query é muito útil para extrair apenas um subconjunto específico de dados da sua coleção para análise ou backup.
