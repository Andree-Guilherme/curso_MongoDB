# Inserindo dados em uma coleção

### Insersão passo a passo
1. Para inserir dados dentro da collection via interface gráfica, clique em __ADD DATA__
2. __Será perguntado se deseja Import JSON or CSV file ou Insert document__
3. Depois, abrirá uma tela onde podemos colocar o documento
4. Existem duas formas de inserir os dados nessa tela, chamadas de __VIEW JSON__ e __VIEW Simplificada__ (linha a linha):

#### VIEW JSON:

* Nesta visão, você insere o documento no formato JSON, que é o padrão
* Pode usar o modelo já preenchido pelo Mongo ou apagar as informações para inserir um novo JSON
* O Mongo gera automaticamente o campo de ID (`_id`), então não é necessário declará-lo manualmente
* A sintaxe para criação do JSON deve seguir o padrão JSON válido para inserção de dados

#### VIEW Simplificada (linha a linha):

* Nesta visão, a inserção é feita campo a campo, como se fosse uma tabela
* Você adiciona os valores e seleciona o tipo de dado para cada campo
* Para adicionar um novo campo, clique no símbolo de +
* Para excluir um campo, clique no ícone de lixeira

5. Após inserir os dados em qualquer uma das views, o Mongo gera um ID automaticamente para o documento inserido
6. Por fim clicar em __Insert__