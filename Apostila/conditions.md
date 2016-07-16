#Condições


As diretivas de controle do LESS permitem a utilização de operadores condicionais e iterações. Neste capítulo serão explicadas as diretivas condicionais `when` e `when not`.

A diretiva `when` recebe uma expressão e caso essa expressão seja diferente de falso algum comando será executado. Para complementar a diretiva `when`, existe a diretiva `when not` que será executada caso as expressões da `when` sejam falsas.

Exemplo:

```

@template: dark;

header {
  when(@template: == dark) {
    color: #fff;
    background: #222;
  }
  when(@template: == light) {
    color: #333;
    background: #fff;
  }
}

```
No exemplo acima, existe uma variável $template e o esquema de cores do seletor header será atribuido de acordo com o valor da variável @template. Neste caso, o esquema de cores atribuido será o primeiro, pois o valor da variável $template é igual a dark.

O CSS compilado será:

```
header {
  color: #fff;
  background: #222;
}
```

___

<p align="center"><a href="functions.md"  title="Anterior"><< Funções</a> | <a href="iteration.md" title="Próximo">Iterações >></a></p>
