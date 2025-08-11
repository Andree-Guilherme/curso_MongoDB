# Excluindo Bancos e coleções

### Excluindo uma collection
1. Para excluir uma collection temos duas maneiras
   1. Na aba lateral esquerda localizamos a collection desejada dentro do banco de dados e clicamos no símbolo de 🗑️
   2. Localizamos a Database dentro do Server Group na lateral esquerda e clicamos sobre ela. Sera exibido uma tela na grid principal contendo as collections, então basta clicar no símbolo de 🗑️ localizado a direita
2. Após escolher um dos meios sera aberto um pop-up de confirmação __Type "{nome_da_collection}" to confirm your action__
3. Por fim clicar em __Drop Collection__

---

### Excluindo um banco de dados
1. Para excluir uma collection temos duas maneiras
   1. Na aba lateral esquerda localizamos a Database desejada dentro do Server Group e clicamos no símbolo de 🗑️
   2. Clicamos no Server Group na aba lateral esquerda, então sera aberta na grid principal todas as Databases. Selecionamos a desejada e clicamos sobre o símbolo de 🗑️ localizado a direita
2. Após escolher um dos meios sera aberto um pop-up de confirmação __Type "{nome_da_database}" to confirm your action__
3. Por fim clicar em __Drop Database__

---

### Excluindo uma collection via shell
1. Abra o terminal
2. Acesso o __mongo shell__ com `mongosh`
2. Para visualizar as coleções, digite `show collections`
3. Para deletar uma coleção, use o comando `db.{nome_da_colecao}.drop()`
4. Importante: se a coleção tiver espaço no nome, use a notação `db["nome da colecao"].drop()`
5. Após a exclusão, o comando retorna __True__
6. Digite `exit` para sair do mongo shell

---

### Excluindo um banco de dados via shell
1. Abra o terminal
2. Acesso o __mongo shell__ com `mongosh`
3. Entre no banco de dados desejado usando `use {nome_do_banco}`
4. Execute o comando `db.dropDatabase()`
5. Será retornado o __status: ok__ e exibido que as coleções dentro dele foram removidas
6. Digite `exit` para sair do mongo shell

---

Por regra, se um banco de dados tiver todas as suas coleções excluídas, ele também será removido, pois é necessário que exista pelo menos uma coleção para que o banco seja mantido.