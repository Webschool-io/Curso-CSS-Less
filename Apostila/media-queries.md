#@media

A diretiva @media funciona no LESS da mesma forma que funciona no CSS, porém há possibilidade de encaixá-las em regras CSS, desta forma é possível declarar dentro do seletor qual será o comportamento dele de acordo com cada @media.

Exemplo:

```

.sidebar {
  width: 30%;
  @media screen and (orientation: landscape) {
     width: 40%;
  }
}

.container {
  width: 90%;
  @media screen and (orientation: landscape) {
     width: 100%;
  }
}

```
A @media é declarada para cada seletor. No momento de compilação todas as regras da mesma @media são unificadas:

```

.sidebar {
   width: 30%;
}

.container {
   width: 90%;
}

@media screen and (orientation: landscape) {
 .sidebar {
    width: 40%;
 }

 .container {
    width: 90%;
 }

}

```

___

<p align="center"><a href="iteration.md" title="Anterior"><< Iterações</a> | <a href="import.md" title="Próximo">@import >></a></p>
