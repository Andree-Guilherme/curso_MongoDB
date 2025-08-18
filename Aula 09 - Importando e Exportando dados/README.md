# 📦 Importar e Exportar Dados no MongoDB Compass

## 📥 Importando dados
1. Abra o **MongoDB Compass** e conecte-se ao seu banco
2. No menu lateral, selecione a **database** e depois a **collection** onde deseja importar 
3. Clique em **Collection → ADD DATA → Import JSON or CSV file** 
4. Escolha o **arquivo a importar**:  
   - Formatos aceitos: **JSON** ou **CSV**
5. Configure as opções de importação
   - Ative ou desative **Stop on Errors** - _se ativado, a importação para ao encontrar o primeiro erro_
6. Clique em **IMPORT** e aguarde
   - Os registros serão adicionados à collection selecionada

---

## 📤 Exportando dados
1. Abra a **collection** que deseja exportar
2. Clique em **Collection → Export Collection**
3. Defina se deseja exportar:  
   - **Todos os documentos**  
   - **Apenas o resultado de uma query filtrada**  
4. Escolha o **formato de exportação** (JSON ou CSV)
5. Selecione o **local para salvar** e clique em **EXPORT**
6. O arquivo será salvo no seu computador