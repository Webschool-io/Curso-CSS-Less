#@import

Através da diretiva @import é possível importar arquivos no seu arquivo principal. Durante o processo de compilação os arquivos importados são unificados gerando um único arquivo CSS. Todas as variáveis ou mixins definidas nos arquivos importados podem ser usados no arquivo principal.

Sintaxe:

```
@import arquivoimportado.less;
```

Por padrão a diretiva @import busca por arquivos LESS, por isso quando se importa arquivos LESS a extensão é opicional. O @import também pode ser utilizado de outras formas:

- Importar arquivos .css.
- Importar arquivo via http://.
- Importar arquivo via url().
- Importar media queries

Exemplos de utilização

```

@import "foo.css";                                  //importando um arquivo CSS
@import "foo" min-width:400px;                      //importa o arquivo CSS quando a tela tem no mínimo 400px
@import "http://foo.com/bar";                       //importa arquivo via http
@import @import url("http://fonts.googleapis.com/css?family=Droid+Sans");  //importa via url()

```

É possível importar vários arquivos de uma só vez:

```
@import "file1", "file2";
```

##Partials

Para organizar melhor o seu projeto, utilizando o import você pode dividir seu CSS em vários pedaços e importar em um arquivo principal. Caso você deseje importar cada arquivo less de estilo específico, mas não quer que toda hora esse arquivo seja compilado para um arquivo separado, basta colocar um _ na frente do nome do arquivo. Isto indicará para o LESS não compilá-lo para um arquivo CSS, este é o conceito de **partials**.

Os partials importados só serão compilados quando o arquivo principal for compilado e seus estilos serão exibidos no arquivo principal.

Exemplo de estrutura de projeto utilizando partials:

```

partials/
        _base.less
        _buttons.less
        _figures.less
        _grids.less
        _typography.less
        _reset.less
style.less

```

Style.less:

```

@import partials/base.less
@import partials/buttons.less
@import partials/figures.less
@import partials/grids.less
@import partials/typography.less
@import partials/reset.less

```

Não é necessário colocar o _ na importação dos arquivos.

___

<p align="center"><a href="media-queries.md.md"  title="Anterior"><< @media</a> | <a href="../Apostila#Índice" title="Índice">Índice</a></p>
