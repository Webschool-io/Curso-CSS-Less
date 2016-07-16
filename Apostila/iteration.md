#Iterações

Para realização de iterações, existe a diretiva .loop .

##.loop

A diretiva .loop pode ser utilizada :


```
.loop(@counter) when (@counter > 0) {
  .loop((@counter - 1));    // next iteration
  width: (10px * @counter); // code for each iteration
}

div {
  .loop(5); // launch the loop
}
```

Será compilado para:

```
div {
  width: 10px;
  width: 20px;
  width: 30px;
  width: 40px;
  width: 50px;
}
```

Um exemplo de uso recursivo do loop.

```
.generate-columns(4);

.generate-columns(@n, @i: 1) when (@i =< @n) {
  .column-@{i} {
    width: (@i * 100% / @n);
  }
  .generate-columns(@n, (@i + 1));
}

```
Será compilado para:

```
.column-1 {
  width: 25%;
}
.column-2 {
  width: 50%;
}
.column-3 {
  width: 75%;
}
.column-4 {
  width: 100%;
}
```

___

<p align="center"><a href="conditions.md"  title="Anterior"><< Condições</a> | <a href="media-queries.md" title="Próximo">@media >></a></p>
