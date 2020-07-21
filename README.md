# Boas vindas ao repositório frontend do projeto de Deploy - Stranger Things!

Aqui você vai encontrar os locais para colocar suas repostas relativas aos requisitos de frontend.

**Lembre-se**: coloque as respostas apenas dos requisitos que contém o seguinte direcionamento:

  - Adicione os comandos utilizados, de maneira sequencial, ao README do frontend.

**Nota**: Este direcionamento está presente no [repositório](https://github.com/tryber/sd-01-project-stranger-things) em que os requisitos do projeto são destrinchados.

## Requisitos

### 9 - Deploy Heroku

Para realizar o deploy do meu frontend, fiz o seguinte procedimento:

heroku create andrey-stranger-things --buildpack mars/create-react-app

heroku config:set \
REACT_APP_HAWKINGS=https://andrey-ts-hawkins.herokuapp.com/ \
REACT_APP_UPSIDE_DOWN=https://andrey-ts-upside-down.herokuapp.com/ \
REACT_APP_TIMEOUT=30000 \
-a andrey-stranger-things

git push heroku andrey-stranger-things:master

## Bônus

### 10 - Multi-ambientes

Para tornar a minha a minha aplicação Multi-ambiente, fiz o seguinte procedimento:

git remote rename heroku development
heroku create --remote production --app andrey-ts-production --buildpack mars/create-react-app

git push production andrey-stranger-things:master
