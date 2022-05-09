### Removendo todos de acordo com o filtro

```db.postagens.remove({ tituloe: "Primeira Postagem" });```

### Removendo apenas um registro de acordo com o filtro

```db.postagens.remove({ titulo: "Segunda Postagem" }, 1);```

### Removendo tudo! Delete sem WHERE

```db.postagens.remove({  });```

### Para deletar a collection

```db.postagens.drop();```

