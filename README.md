# Boas vindas ao repositório frontend do projeto de Deploy - Stranger Things!

Aqui você vai encontrar os locais para colocar suas repostas relativas aos requisitos de frontend.

**Lembre-se**: coloque as respostas apenas dos requisitos que contém o seguinte direcionamento:

- Adicione os comandos utilizados, de maneira sequencial, ao README do frontend.

**Nota**: Este direcionamento está presente no [repositório](https://github.com/tryber/sd-01-project-stranger-things) em que os requisitos do projeto são destrinchados.

## Requisitos

### 9 - Deploy Heroku

heroku create --buildpack mars/create-react-app;
heroku create --remote hawkins stranger-things-bolivar-front --buildpack mars/create-react-app;
heroku create --remote upside-down stranger-things-bolivar-frontd --buildpack mars/create-react-app;
git remote -v;

heroku config:set URL=https://stranger-things-bolivar-front.herokuapp.com/ TIMEOUT=3000 PM2_PUBLIC_KEY=yv16rnirig4y70n PM2_SECRET_KEY=ehot5qk1n1khzlu PM2_MACHINE_NAME=andersonbolivar-15aa --app stranger-things-bolivar-front;

heroku config:set URL=https://stranger-things-bolivar-frontd.herokuapp.com/ TIMEOUT=5000 PM2_PUBLIC_KEY=yv16rnirig4y70n PM2_SECRET_KEY=ehot5qk1n1khzlu PM2_MACHINE_NAME=andersonbolivar-15aa --app stranger-things-bolivar-frontd;

git push hawkins bolivar-stranger-things-frontend:master;

git push upside-down bolivar-stranger-things-frontend:master;

## Bônus

### 10 - Multi-ambientes

git remote rename hawkins development;

git remote rename upside-down production;

heroku config:set NODE_ENV=development --app stranger-things-bolivar-front;

heroku config:set NODE_ENV=production --app stranger-things-bolivar-frontd;

git push development bolivar-stranger-things-frontend:master;

https://stranger-things-bolivar-front.herokuapp.com/;

git push production bolivar-stranger-things-frontend:master;

https://stranger-things-bolivar-frontd.herokuapp.com/;

### 6 - Deploy Heroku

git status: On branch bolivar-stranger-things-backend;

- Login no Heroku

  - heroku login;

- Remotes:

  - heroku create --remote hawkins stranger-things-bolivar;
  - heroku create --remote upside-down stranger-things-bolivar-down;
  - git remote -v;

- Variáveis de Ambiente:

  - heroku config:set
    upsideDown="false"
    PM2_PUBLIC_KEY=PUBLIC_KEY
    PM2_SECRET_KEY=SCRECT_KEY
    PM2_MACHINE_NAME=andersonbolivar-15aa
    --app stranger-things-bolivar;
  - heroku config:set
    upsideDown="true"
    PM2_PUBLIC_KEY=yv16rnirig4y70n
    PM2_SECRET_KEY=ehot5qk1n1khzlu
    PM2_MACHINE_NAME=andersonbolivar-15aa
    --app stranger-things-bolivar-down;

- Deploy:

  - git add;
  - git commit -m "BOLIVAR"
  - git push hawkins bolivar-stranger-things-backend:master;
  - git push upside-down bolivar-stranger-things-backend:master;

### 7 - Monitoramento

- Logs:

  - heroku logs --tail --app stranger-things-bolivar;
  - heroku logs --tail --app stranger-things-bolivar-down;
  - heroku apps:info stranger-things-bolivar;
  - heroku apps:info stranger-things-bolivar-down
