# 🗑️ Excluindo Bancos e Coleções

---

## 🔹 Excluindo uma collection

1. Existem duas maneiras de excluir uma collection:
   1. Na **aba lateral esquerda**, localize a collection desejada dentro do banco e clique no símbolo de 🗑️.
   2. Localize a **Database** dentro do **Server Group** na lateral esquerda e clique sobre ela. Na grid principal, serão exibidas todas as collections; clique no símbolo de 🗑️ à direita da collection desejada.
2. Um **pop-up de confirmação** será exibido:  
   > Type "{nome_da_collection}" to confirm your action
3. Clique em **Drop Collection** para concluir.

---

## 🔹 Excluindo um banco de dados

1. Existem duas maneiras de excluir um banco:
   1. Na **aba lateral esquerda**, localize a Database desejada dentro do Server Group e clique no símbolo de 🗑️.
   2. Clique no **Server Group** na aba lateral esquerda. Na grid principal, selecione a Database desejada e clique no símbolo de 🗑️ à direita.
2. Um **pop-up de confirmação** será exibido:  
   > Type "{nome_da_database}" to confirm your action
3. Clique em **Drop Database** para concluir.

---

## 💻 Excluindo uma collection via Shell

1. Abra o terminal.
2. Acesse o **mongo shell** com:  
   <pre><code>mongosh</code></pre>
3. Para visualizar as coleções:  
   <pre><code>show collections</code></pre>
4. Para deletar uma coleção:  
   <pre><code>db.{nome_da_colecao}.drop()</code></pre>
5. Se o nome da coleção tiver espaços, use:  
   <pre><code>db["nome da colecao"].drop()</code></pre>
6. Após a exclusão, o comando retorna **true**.
7. Digite `exit` para sair do shell.

---

## 💻 Excluindo um banco de dados via Shell

1. Abra o terminal.
2. Acesse o **mongo shell** com:  
   <pre><code>mongosh</code></pre>
3. Entre no banco desejado:  
   <pre><code>use {nome_do_banco}</code></pre>
4. Execute o comando para excluir o banco:  
   <pre><code>db.dropDatabase()</code></pre>
5. Será retornado o **status: ok** e exibido que todas as collections foram removidas.
6. Digite `exit` para sair do shell.

---

> ⚠️ Por regra, se um banco tiver todas as suas collections excluídas, ele também será removido, pois é necessário que exista **pelo menos uma collection** para que o banco seja mantido.
