# Boas vindas ao repositório frontend do projeto de Deploy - Stranger Things!

Aqui você vai encontrar os locais para colocar suas repostas relativas aos requisitos de frontend.

**Lembre-se**: coloque as respostas apenas dos requisitos que contém o seguinte direcionamento:

  - Adicione os comandos utilizados, de maneira sequencial, ao README do frontend.

**Nota**: Este direcionamento está presente no [repositório](https://github.com/tryber/sd-01-project-stranger-things) em que os requisitos do projeto são destrinchados.

## Requisitos

### 9 - Deploy Heroku

Para realizar o deploy do meu frontend, fiz o seguinte procedimento:

`Adicione aqui os comandos utilizados, de maneira sequencial.`

heroku create stranger-things-trybe01 --buildpack mars/create-react-app
git remote rename front-domain
heroku config:set URL="https://floating-fortress-36656.herokuapp.com/" --app stranger-things-trybe01
heroku config:set URLDOWN="https://obscure-basin-84879.herokuapp.com/" --app stranger-things-trybe01
heroku config:set CONFIG="30000" --app stranger-things-trybe01
heroku config:set DOWNCONFIG="30000" --app stranger-things-trybe01
git push front-domain douglas-he-stranger-things:master


## Bônus

### 10 - Multi-ambientes

Para tornar a minha a minha aplicação Multi-ambiente, fiz o seguinte procedimento:

`Adicione aqui os comandos utilizados, de maneira sequencial.`
