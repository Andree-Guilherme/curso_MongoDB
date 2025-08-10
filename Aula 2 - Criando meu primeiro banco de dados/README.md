# Criando meu primeiro banco de dados

### Conectando ao banco
1. Para criar um banco de dados, primeiro devemos nos conectar a ele clicando em __Add new connection__
2. Depois ira aparecer a tela de __New Connection__ onde definiremos a __URI (String de Conexão)__
3. Dexaremos a URI padrão `mongodb://localhost:27017/`
4. Salvar as informações
   1. __Save:__ Salva as configurações ou dados atuais
   2. __Connect:__ Sempre vai ter que clicar em conectar, independente de já ter salvo ou não
   3. __Save & Connect:__ Não exige reconexão manual toda vez, porque você pode simplesmente reabrir a conexão salva e entrar direto
5. Feito isso já estamos conectados no servidor local
---
### Criando o banco
1. Ao se conectar, por padrão já vai vir criado 3 bancos de dados
   1. __admin__ - _Banco administrativo que armazena credenciais, roles e configurações de nível global_
   2. __config__ - _Usado pelo sharding para guardar metadados e informações de configuração dos shards_
   3. __local__ - _Guarda dados locais do nó, como informações de replicação; não é replicado entre servidores_
2. Para criar um novo banco de dados basta clicar no botão __Create database__
3. Ao clicar em __Create database__ será aberto uma tela indicando para preencher
* __Database Name__
* __Collection Name__

__Por padrão na criação sempre tem que ter uma collection já criada__

_Em analogia ao banco de dados relacional uma collection seria uma tabela, mas não é_

4. Por fim clicar em __Create Database__
---
### Criando o banco via Shell
1. Abrimos o `CMD` e digitamos `mongosh` para se __conectar ao banco de dados__

__Importante:__ Ao se conectar ao banco de dados ele mostra
* __O caminho em que esta se conectando__
* __A versão do mongoDB__
* __A versão do shell__
2. Para __exibir os bancos de dados existentes__ digitamos o comando `show databases`
3. Para __criar um novo banco__ de dados usamos o comando:
   1. `use{nome_do_banco}`
   2. `db.createCollection("{nome_da_collecion}")`

* O primeiro comando trocara o banco de dados mesmo que ainda não esteja criado
* Respeitando a regra do banco sempre temos que criar uma collection junto com o banco por isso não adianta apenas trocar o banco, temos que passar o segundo comando também

4. Sera retornado uma mensagem de __ok__
5. Banco de dados criado

__O comando `use` também serve para alterar entre os bancos de dados já existentes__

_O mongo é case sensitive, ou seja, devemos digitar os comandos e bancos de forma correta_