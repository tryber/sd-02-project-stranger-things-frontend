# Boas vindas ao repositório frontend do projeto de Deploy - Stranger Things!

Aqui você vai encontrar os locais para colocar suas repostas relativas aos requisitos de frontend.

**Lembre-se**: coloque as respostas apenas dos requisitos que contém o seguinte direcionamento:

  - Adicione os comandos utilizados, de maneira sequencial, ao README do frontend.

**Nota**: Este direcionamento está presente no [repositório](https://github.com/tryber/sd-01-project-stranger-things) em que os requisitos do projeto são destrinchados.

## Requisitos

### 9 - Deploy Heroku

Para realizar o deploy do meu frontend, fiz o seguinte procedimento:

heroku create --remote heroku stranger-things-frontend-123 --buildpack mars/create-react-app

heroku config:set REACT_APP_HAWKINS=https://stranger-things-216987.herokuapp.com REACT_APP_TIMEOUT_HAWKINS=30000 REACT_APP_UPSIDE_DOWN=https://stranger-things-216988.herokuapp.com REACT_APP_TIMEOUT_UPSIDE_DOWN=30000 --app stranger-things-frontend-123

git push heroku mateus-stranger-things-frontend:master 

## Bônus

### 10 - Multi-ambientes

Para tornar a minha a minha aplicação Multi-ambiente, fiz o seguinte procedimento:

`Adicione aqui os comandos utilizados, de maneira sequencial.`
git remote rename heroku development