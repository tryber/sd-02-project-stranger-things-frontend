# Boas vindas ao repositório frontend do projeto de Deploy - Stranger Things!

Aqui você vai encontrar os locais para colocar suas repostas relativas aos requisitos de frontend.

**Lembre-se**: coloque as respostas apenas dos requisitos que contém o seguinte direcionamento:

  - Adicione os comandos utilizados, de maneira sequencial, ao README do frontend.

**Nota**: Este direcionamento está presente no [repositório](https://github.com/tryber/sd-01-project-stranger-things) em que os requisitos do projeto são destrinchados.

## Requisitos

### 9 - Deploy Heroku

Para realizar o deploy do meu frontend, fiz o seguinte procedimento:

`Adicione aqui os comandos utilizados, de maneira sequencial.`

```
$ heroku create --remote heroku-st front-st --buildpack mars/create-react-app

$ heroku config:set REACT_APP_normalWorld=https://stranger-things.herokuapp.com/ REACT_APP_upsideDown=https://stranger-things-up-down.herokuapp.com/ REACT_APP_timeout=30000 --app front-st

$ git add .
$ git commit -m "Requisito 9"
$ git push heroku-st pedro-tofani:master

```

## Bônus

### 10 - Multi-ambientes

Para tornar a minha a minha aplicação Multi-ambiente, fiz o seguinte procedimento:

`Adicione aqui os comandos utilizados, de maneira sequencial.`
