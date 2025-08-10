# Como Instalar o MongoDB

### Download MongoDB e Compass
1. Acessamos o site [mongodb](https://www.mongodb.com/try/download/community)
2. Em seguida achamos a parte de Download
3. Selecionamos os seguintes campos:
   1.  Version
   2.  Plataform
   3.  Package
4.  Por fim clicamos em __Download__

### Download MongoDB Shell
1. Acessamos o site [mongosh](https://www.mongodb.com/try/download/shell)
2. Selecionamos os seguintes campos:
   1.  Version
   2.  Plataform
   3.  Package
__Certifique-se de escolher a mesma versão da instalação gráfica para manter a compatibilidade__
4.  Por fim clicamos em __Download__

### Instalando o MongoDB
1. Execute o instalador como administrador
2. Clique em __Next__
3. Aceite os termos do contrato
- [X] I accept the terms in the License Agreement
4. Escolha o tipo de instalação
   1. Completa - _mais utilizada_
   2. Customizada
5. Escolher a instalação completa
6. Sera aberto a tela de configuração do serviço - __deve ser usado as seguintes opções:__
- [X] Install MongoD as a Service
- [X] Run service as Network Service user
* Service Name: {nome_do_serviço}
* Data Directory: {definir_diretorio_de_dados}
* Log Directory: {definir_diretorio_de_log}
7. Clique em __Next__
8. A próxima tela perguntará se deseja instalar a interface gráfica MongoDB Compass
- [X] Install MongoDB Compass - _marque essa opção_
9. Clique em __Next__
10. Clique em __Install__ e aguarde o carregamento
11. Clique em __Finish__ para concluir a instalação
__Recomenda-se reiniciar o computador após o termino__

### Instalando Mongo Shell
1. Execute o instalador como administrador
2. Escolha o local de instalação
3. Defina se deseja instalar apenas para o seu usuário
- [X] Install just for you - _desmarque essa opção_
4. Clique em __Install__ e aguarde o carregamento
5. Clique em __Finish__ para concluir a instalação
__Recomenda-se reiniciar o computador após o termino__