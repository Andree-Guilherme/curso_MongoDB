# Consultando dados via MongoDB Compass

### Como fazer uma busca
1. Acessar o MongoDB Compass
2. Localizar a Query Bar
   1. Por pardrão já sera apresentando o __{ }__
3. Dentro do campo de busca podemos buscar por uma chave e valor
   1. `{<"key">: <value>}`

* Caso o filtro esteja errado o botão __Find__ não sera habilitado

---

### Filtro Project
1. Acessar o MongoDB Compass
2. Localizar o filtro __Project__
   1. Por pardrão já sera apresentando o __{ }__
3. Dentro do campo de busca podemos filtrar apenas as chaves e valores desejados
    1. `{<key>: 1}` || `{<key>: 0}`

* Se o value estiver = 1 o resultado será exibido
* Se o value estiver = 0 o resultado será ocultado

---

### Filtro Sort
1. Acessar o MongoDB Compass
2. Localizar o filtro __Sort__
   1. Por pardrão já sera apresentando o __{ }__
3. Dentro do campo de busca podemos filtrar apenas as chaves e valores desejados
    1. `{<key>: 1}` || `{<key>: -1}`

* Se o value estiver = 1 sera ordenado de A à Z (ascendente)
* Se o value estiver = 0 sera ordenado de Z a A (descendente)

### Filtro Collation
1. Acessar o MongoDB Compass
2. Localizar o filtro __Collation__
   1. Por pardrão já sera apresentando o __{ }__
3. Dentro do campo de busca podemos filtrar por 2 parametros
   1. `locale: <idioma>`
   2. `strength: 2`

* Se o value estiver = 1 sera ordenado de A à Z (ascendente)
* Se o value estiver = 0 sera ordenado de Z a A (descendente)