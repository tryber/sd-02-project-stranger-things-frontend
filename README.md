# Boas vindas ao repositório frontend do projeto de Deploy - Stranger Things!

Aqui você vai encontrar os locais para colocar suas repostas relativas aos requisitos de frontend.

**Lembre-se**: coloque as respostas apenas dos requisitos que contém o seguinte direcionamento:

- Adicione os comandos utilizados, de maneira sequencial, ao README do frontend.

**Nota**: Este direcionamento está presente no [repositório](https://github.com/tryber/sd-01-project-stranger-things) em que os requisitos do projeto são destrinchados.

## Requisitos

### 9 - Deploy Heroku

git status: On branch bolivar-stranger-things-backend;

- Login no Heroku

  - heroku login;

- Remotes:

  - heroku create
    --remote hawkins
    stranger-things-bolivar-dev
    --buildpack mars/create-react-app;
  - git remote -v;

- Variáveis de Ambiente:

  - heroku config:set
    URL=https://stranger-things-bolivar.herokuapp.com/
    TIMEOUT=3000
    PM2_PUBLIC_KEY=yv16rnirig4y70n
    PM2_SECRET_KEY=ehot5qk1n1khzlu
    PM2_MACHINE_NAME=andersonbolivar-15aa
    --app stranger-things-bolivar-dev;

- Deploy:

  - git add;
  - git commit -m "BOLIVAR"
  - git push hawkins bolivar-stranger-things-frontend:master;

## Bônus

### 10 - Multi-ambientes

git remote rename hawkins development;

heroku config:set NODE_ENV=development --app stranger-things-bolivar-dev;

heroku create --remote production stranger-things-bolivar-prod;

heroku config:set URL=https://stranger-things-bolivar-down.herokuapp.com/ TIMEOUT=3000 NODE_ENV=production PM2_PUBLIC_KEY=yv16rnirig4y70n PM2_SECRET_KEY=ehot5qk1n1khzlu PM2_MACHINE_NAME=andersonbolivar-15aa --app stranger-things-bolivar-prod;

git push production bolivar-stranger-things-frontend:master;
