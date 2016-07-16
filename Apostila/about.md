# Sobre Less

O pré-processador LESS foi criado em 2009 por Alexis Sellier e escrito em Ruby mas logo em seguida foi portado para JavaScript.
A grosso modo, o LESS estende o CSS, fornecendo mecanismos disponíveis em linguagens de programação mais tradicionais que não estão disponíveis no CSS, através destes mecanismos, como variáveis, loops, funções e etc, é possível produzir o código de forma rápida, com manutenção fácil, prática e de baixo custo.

A implementação oficial do LESS é open-source e codificada em JavaScrit, no entanto, existem várias implementações em outras linguagens como Python, Java, PHP, JavaScript e muitas outras. Neste curso utilizaremos o módulo lessc do Node, para compilar nossos arquivos LESS.


## Pré-Processador

O Less precisa ser pré-processado antes de gerar o CSS que será renderizado pelo navegador, logo, o navegador nunca renderiza o código Less diretamente a não ser utilizando o less.js porem vamos utilizar o lessc, este módulo compila o arquivo Less e salva o resultado em um arquivo CSS que será renderizado pelo navegador.


## Instalação

Para utilizar o módulo lessc, você precisa do Node.js instalado no seu computador.

```
sudo apt-get install nodejs
```

A seguir instalaremos o gerenciador de pacotes npm, ele permitirá instalar facilmente módulos e pacotes para utilizar com o Node.js.

```
sudo apt-get install npm
```

Finalmente instalamos o lessc globalmente

```
npm install -g less
```

Agora o ambiente está pronto para utilizarmos o Less!


## .less

Você pode usar o Less com a sintaxes: o .less, funciona como o CSS, usando chaves para denotar blocos de código e ponto e vírgula para separar linhas dentro de um bloco.

Observe os exemplos abaixo:

.less
```
body {
  color: #333;
}
```

## Criando um arquivo Less

Para criar um arquivo Less, basta criar um novo arquivo e salvá-lo com a extensão .less. Utilize o bloco abaixo para seguir o primeiro exemplo, salve como exemplo1.less.

```
body {
  color: #333;
}
```


## Compilando um arquivo Less

Você pode compilar um arquivo por vez ou uma pasta, entenda o comando.

```
lessc entrada saída
```

Vamos compilar nosso exemplo:

```
lessc exemplo1.less exemplo1.css
```

___

<p align="center"><a href="../Apostila#Índice" title="Índice">Índice</a> | <a href="selectors.md" title="Próximo">Seletores >></a></p>
