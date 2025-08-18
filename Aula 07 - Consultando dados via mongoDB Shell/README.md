# Consultando dados via mongoDB Shell

### </> Open Export to Language
Ao clicar nessa opção os parametros de busca da Query são automaticamente convertidos para alguma das linguagens de programação disponiveis no mongo

---

### Parametro de busca 

1. Apenas filtro
db.users.find({ <"key">: <"value"> });

2. Filtro + Projeção
db.users.find(
  { <"key">: <"value"> }
).projection({ <"key">: 0 });

3. Filtro + Ordenação
db.users.find({ <"key">: <"value"> })
        .sort({ <"key">: -1 });

4. Filtro + Collation
db.users.find({ <"key">: <"value"> })
        .collation({ locale: "pt", strength: 2 });

5. Filtro + Index Hint
db.users.find({ <"key">: <"value"> })
        .hint({ <"key">: 1 });

6. Filtro + Projeção + Ordenação
db.users.find(
  { <"key">: <"value"> }
).projection({ <"key">: 0, <"key">: 0 })
.sort({ <"key">: -1 });

7. Filtro + Ordenação + Collation
db.users.find({ <"key">: <"value"> })
        .sort({ <"key">: 1 })
        .collation({ locale: "pt", strength: 1 });

8. Filtro + Projeção + Collation
db.users.find(
  { <"key">: <"value"> }
).projection({ <"key">: 0 })
.collation({ locale: "pt", strength: 2 });

9. Filtro + Index Hint + Ordenação
db.users.find({ <"key">: { $gte: <"value"> } })
        .hint({ <"key">: 1 })
        .sort({ <"key">: -1 });

10. Filtro + Projeção + Ordenação + Collation + Index Hint
db.users.find(
  { <"key">: <"value"> }
).projection({ <"key">: 0, <"key">: 0 })
.sort({ <"key">: 1 })
.collation({ locale: "pt", strength: 2 })
.hint({ <"key">: 1 });
