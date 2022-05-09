```db.postagens.insert({ titulo: "Primeira Postagem", conteudo: 'Conteudo 01', tags: [] });```

```db.postagens.insert({ titulo: "Segunda Postagem", conteudo: 'Conteudo 02', tags: [] });```

```db.postagens.insert({ titulo: "Terceira Postagem", conteudo: 'Conteudo 03', tags: ['esporte', 'cinema', 'praia'] });```

### Limitando a consulta a 1 documento

```db.postagens.find().limit(1).pretty();```

### Ordenando crescente

```db.postagens.find().sort({ titulo: 1 });```

### Ordenando descrescente

```db.postagens.find().sort({ titulo: -1 });```

### Realizar projeção de atributos (escolher quais atributos aparecem)

```db.postagens.find({}, { titulo: true, tags: true });```

```db.postagens.find({}, { _id: false, titulo: true });```

### Utilizando IN em campos de vetor

```db.postagens.find({ tags: { $in: ['praia'] } });```