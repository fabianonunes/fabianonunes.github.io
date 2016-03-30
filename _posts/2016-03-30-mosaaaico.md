---
published: true
title: mosaaaico
layout: post
---

## Windows

### Pré-requisitos

#### git

Em vez do `git-bash`, recomendo o terminal [cmder](http://cmder.net). Baixe a versão [full](https://github.com/cmderdev/cmder/releases/download/v1.2.9/cmder.7z) e descompacte em algum diretório no disco rígido (diretamente em `C:\cmder` é uma boa pedida!)

#### node

Da mesma forma que o `Java` precisa da JRE; o `C#`, do .Net CLR; e o `python` do CPython; o `javascript` também exige um runtime: o [Node.js](http://nodejs.org).

A instalação é bem simples: baixe a versão _stable_ adequada a sua arquitetura (32 ou 64 bits) em [https://nodejs.org/en/download/stable/](https://nodejs.org/en/download/stable/).

#### npm

O `npm` é o gerenciador de pacotes do `Node`. É instalado automaticamente junto com o _runtime_.

Assim como qualquer outro gerenciador de pacotes, é lento. Se o `Maven` baixa metada da internet, não se preocupe: o `npm` vai baixar a outra.

Se preferir, utilize como registro uma instância do [local-npm](https://github.com/nolanlawson/local-npm) disponível em `http://mp1522:5080`:

```
npm set registry http://mp1522:5080
```

Para reverter:

```
npm set registry https://registry.npmjs.org
```

## Proxy

Você tá atrás de um proxy? Cara, que azar.

Só tem uma coisa pior que estar atrás de um proxy: estar atrás de um proxy **autenticado**.

😭

É a vida.

Execute (win + R) `SystemPropertiesAdvanced`. Em _Variáveis de Sistema_, adicione as variáveis de sistema HTTP_PROXY e HTTPS_PROXY.

Se o teu proxy é autenticado, ele precisa estar na forma `http://user:password@server:port`. Mas calma, talvez você não precise colocar a **sua** senha ali. Veja se existe alguma conta de desenvolvimento disponível.

Ah, a vantagem de utilizar uma instância do [local-npm](https://github.com/nolanlawson/local-npm) como registro, é que esse passo pode ser desconsiderado.


## grunt e yo

O `grunt` é uma ferramenta de build. É como se fosse um `make`, um `ant`, um `rake` ou as recipes do `buildout`.

Já o `yo` ([Yeoman](http://yeoman.io)) é um gerador de projetos. Ele monta a estrutura de arquivos e diretórios de acordo com um template. É análogo aos _archetypes_ do `Maven` ou o `paster` do python.

Para instalar o `grunt`, o `yo` e o template do `mosaaaico`, execute:

```
npm -g install yo grunt-cli generator-mosaaaico
```


## crie um novo projeto

```bash
mkdir meu_projeto_novo
cd meu_projeto_novo
yo mosaaaico
```
Feito. A seguinte estrutura será gerada:

```
.
├── app
│   ├── assets
│   │   └── logo.svg
│   ├── index.jade
│   ├── less
│   │   ├── main.less
│   │   ├── utils
│   │   │   └── variables.less
│   │   └── vendors
│   │       ├── bootstrap.less
│   │       └── senado.less
│   ├── scripts
│   │   └── main.js
│   └── senado.jade
├── grunt
│   ├── aliases.yaml
│   ├── autoprefixer.js
│   ├── clean.js
│   ├── concurrent.js
│   ├── connect.js
│   ├── copy.js
│   ├── cssmin.js
│   ├── jade.js
│   ├── less.js
│   └── watch.js
├── Gruntfile.js
└── package.json
```

Para rodar o servidor embutido, execute no diretório `grunt dev`. A porta escolhida por padrão é a 8000. Se precisar alterar, passe o argumento `--port=`.

A interface utilizada é a 127.0.0.1. Se precisar liberar acesso externo, passe o argumento `--allow-remote`.


```
grunt dev --port=9090 --allow-remote
```
