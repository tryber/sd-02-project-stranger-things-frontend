# Boas vindas ao repositório frontend do projeto de Deploy - Stranger Things!

Aqui você vai encontrar os locais para colocar suas repostas relativas aos requisitos de frontend.

**Lembre-se**: coloque as respostas apenas dos requisitos que contém o seguinte direcionamento:

  - Adicione os comandos utilizados, de maneira sequencial, ao README do frontend.

**Nota**: Este direcionamento está presente no [repositório](https://github.com/tryber/sd-01-project-stranger-things) em que os requisitos do projeto são destrinchados.

## Requisitos

### 9 - Deploy Heroku

Para realizar o deploy do meu frontend, fiz o seguinte procedimento:

```
heroku create --remote heroku lauro-st --buildpack mars/create-react-app

heroku config:set REACT_APP_normalWorld=https://lauro-stranger-things.herokuapp.com/ REACT_APP_upsideDown=https://lauro-stranger-things-reverse.herokuapp.com/ REACT_APP_timeout=30000 --app lauro-st

git add .
git commit -m "Req. 9"
git push heroku lauro-stranger-things:master
```

## Bônus

### 10 - Multi-ambientes

Para tornar a minha a minha aplicação Multi-ambiente, fiz o seguinte procedimento:

`Adicione aqui os comandos utilizados, de maneira sequencial.`
