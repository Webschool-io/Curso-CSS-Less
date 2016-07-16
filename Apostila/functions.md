#Funções

O LESS possui algumas funções nativas e também possibilita que sejam criadas novas funções.

##Criando uma função

A declaração de uma função começa com @function, em seguida vem o nome da função, que pode conter qualquer combinação de caracteres alfabéticos e numéricos sem espaços, os argumentos entre parênteses e a definição da função entre chaves.

As funções podem acessar quaisquer variáveis definidas globalmente. Uma função pode ter várias declarações contidas dentro dela, é necessário utilizar o @return para definir o valor de retorno da função.

```
@calc-fluid(@target, @container) {
  return (@target / @container) * 100%;
}
```

##Utilizando uma função

Para utilizar uma função basta colocar o nome e passar os argumentos:

```
div {
  width: @calc-fluid(650px, 1000px);
}
```

Será compilado para:

```
div {
  width: 65%;
}
```

##Funções Nativas

Nesta apostila serão mostradas algumas das principais funções nativas do LESS. É possível consultar uma lista com todas as funções nativas no site do <a href="http://lesscss.org/functions/#functions-overview" target="_blank">LESS</a>.

___

<p align="center"><a href="mixins.md"  title="Anterior"><< Mixins</a> |  <a href="conditions.md" title="Próximo">Condições >></a></p>
