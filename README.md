# Boas vindas ao repositório frontend do projeto de Deploy - Stranger Things!

Aqui você vai encontrar os locais para colocar suas repostas relativas aos requisitos de frontend.

**Lembre-se**: coloque as respostas apenas dos requisitos que contém o seguinte direcionamento:

  - Adicione os comandos utilizados, de maneira sequencial, ao README do frontend.

**Nota**: Este direcionamento está presente no [repositório](https://github.com/tryber/sd-01-project-stranger-things) em que os requisitos do projeto são destrinchados.

## Requisitos

### 9 - Deploy Heroku

Para realizar o deploy do meu frontend, fiz o seguinte procedimento:

 `heroku create rw-st-frontend --buildpack mars/create-react-app`
 
 `heroku config:set REACT_APP_STRANGER_THINGS_CONFIG=http://richard-st-hawkings.herokuapp.com/ REACT_APP_UPSIDE_DOWN_CONFIG=http://richard-st-upsidedown.herokuapp.com/ REACT_APP_TIMEOUT=30000 -a rw-st-frontend`
 
 `heroku config -a rw-st-frontend`
 
 `git remote rename heroku front`
 
 `git push front feature/frontend:master`

 Link Deploy: https://rw-st-frontend.herokuapp.com/

## Bônus

### 10 - Multi-ambientes

Para tornar a minha a minha aplicação Multi-ambiente, fiz o seguinte procedimento:

`Adicione aqui os comandos utilizados, de maneira sequencial.`
