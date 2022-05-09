### Fazendo update na collection de ```postagens```, alterando os documentos onde o ```titulo``` seja igual a ```Primeira Postagem```. Setando o valor do atributo ```conteudo``` para ser igual a ```Conteudo alterado pelo update```

```db.postagens.update({ titulo: "Primeira Postagem" }, { $set: { conteudo: "Conteudo alterado pelo update" } });```

### Alterando um atributo de um documento dentro de um documento. É preciso usar as aspas ```"caracteristicas.cor"```

```db.postagens.update({ titulo: "Quarta Postagem" }, { $set: { "caracteristicas.cor": "azul" } });```

### Atualizando múltiplos documentos

```db.postagens.update({ titulo: { $regex: /Postagem/ } }, { $set: { "caracteristicas.cor": "laranja" } }, { multi: true });```

### Substituindo todo o documento. Não precisa utilizar o ```$set```

```db.postagens.update({ titulo: "Segunda Postagem" }, { titulo: "Segunda Postagem Atualizada", conteudo: "Conteúdo atualizado da segunda postagem", tags: [], caracteristicas: { cor: "sua favorita" } });```