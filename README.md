# Seja bem-vindo(a) à minha branch de deploy do projeto Stranger Things Front-End, siga os passos corretamente e divirta-se.
---
# Passo 1:

* Crie sua aplicação, utilize o terminal já na pasta clonada do projeto.
* Execute o seguinte comando:

      heroku create nome-aleatório-aqui --buildpack mars/create-react-app

* O heroku criará um endereço com esse nome aleatório,
* Exemplo: https://nome-aleatório-aqui.herokuapp.com/
* Se o nome já existir o heroku create dará erro. Escolha um nome único ou então apenas dê o comando:

      heroku create --buildpack mars/create-react-app

* O heroku irá gerar um nome aleatório inexistente para seu app.
---
# Passo 2:

* Após a criação do app verifique com 'git remote -v' se o remote 'heroku' foi criado.
---
# Passo 3:

* Criar uma branch é opcional, isso pode te ajudar a gerir todas as alterações sem afetar a master.
* Mas para fins didáticos você pode pular a etapa de criação de branch abaixo:
---
* Crie sua branch com o comando:

      git checkout -b nome-da-sua-branch

---

* Agora voce está na branch de desenvolvimento, ou caso tenha pulado a etapa de criação,
* Você estará na branch <strong>master</strong>.
---
# Passo 4:

* Commite as informações e envie ao heroku:

      git add .
      git commit -m "Iniciando deploy"
      git push heroku nome-da-sua-branch:master

* Caso não tenha criado uma branch, após commitar, apenas dê o comando:
      
      git push heroku master

* Feito isso sua aplicação estará no ar com o endereço:

* https://nome-do-seu-app-aqui.herokuapp.com

* Você pode verificar o nome dos seus apps com o comando:

      heroku apps
---
# Passo 6:

* ## Criando variavéis de ambiente

* Seu app ainda não estará disponível, pois o código espera algumas variáveis de ambiente.
* Com seu APP Criado, precisaremos defini-las para rodar nossa aplicação.
* Nas <strong>linha 9, 10, 14 e 15</strong> do arquivo <strong>StrangerThings.js</strong> na pasta <strong>components</strong> temos algumas variáveis ambiente pra  configurar no heroku.
* Vamos definir essas variáveis ambiente no heroku através do terminal.
* Insira o seguinte comandos com as devidas substituições para definir a variável da <strong>linha 9</strong>:

      heroku config:set REACT_APP_NORMAL_ENDPOINT="endereço-do-endpoint-normal-aqui" --app nome-do-seu-app-front-end

* Insira o seguinte comandos com as devidas substituições para definir a variável da <strong>linha 10 e 15</strong>:

      heroku config:set REACT_APP_TIMEOUT="30000" --app nome-do-seu-app-front-end

* Insira o seguinte comandos com as devidas substituições para definir a variável da <strong>linha 14</strong>:

      heroku config:set REACT_APP_INVERSE_ENDPOINT="endereço-do-endpoint-invertido-aqui" --app nome-do-seu-app-front-end

---
* ## Prontinho, sua aplicação já está pronta e realizando as requisições nos endpoints criados no Back-End.

---
# Parabéns, você realizou deploy da aplicação.
