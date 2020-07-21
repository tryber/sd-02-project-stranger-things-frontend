# Boas vindas ao repositório frontend do projeto de Deploy - Stranger Things!

Aqui você vai encontrar os locais para colocar suas repostas relativas aos requisitos de frontend.

**Lembre-se**: coloque as respostas apenas dos requisitos que contém o seguinte direcionamento:

  - Adicione os comandos utilizados, de maneira sequencial, ao README do frontend.

**Nota**: Este direcionamento está presente no [repositório](https://github.com/tryber/sd-01-project-stranger-things) em que os requisitos do projeto são destrinchados.

## Requisitos

### 9 - Deploy Heroku

Para realizar o deploy do meu frontend, fiz o seguinte procedimento:

`heroku create --remote stranger-things guicgs-stranger-things --buildpack mars/create-react-app`

`heroku config:set REACT_APP_HAWKINS_API=https://guicgs-st-backend.herokuapp.com/ --remote stranger-things`

`heroku config:set REACT_APP_UPSIDE_DOWN_API=https://guicgs-st-backend-upside.herokuapp.com/ --remote stranger-things`

`heroku config:set REACT_APP_API_TIMEOUT=30000 --remote stranger-things`

`git push stranger-things guicgs-stranger-things-frontend:master`


## Bônus

### 10 - Multi-ambientes

Para tornar a minha a minha aplicação Multi-ambiente, fiz o seguinte procedimento:

`git remote rename stranger-things production`

`heroku create --remote development guicgs-stranger-things-dev --buildpack mars/create-react-app`

`heroku config:set REACT_APP_HAWKINS_API=https://guicgs-st-backend.herokuapp.com/ --remote development`

`heroku config:set REACT_APP_UPSIDE_DOWN_API=https://guicgs-st-backend-upside.herokuapp.com/ --remote development`

`heroku config:set REACT_APP_API_TIMEOUT=30000 --remote development`

`git push development guicgs-stranger-things-frontend:master`
