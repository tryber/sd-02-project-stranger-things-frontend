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
* Insira os seguinte comandos:

      heroku config:set UP_DOWN=false --app nome-do-seu-app-aqui

* Ao inserir o comando sua aplicação será reiniciada, e ao acessar o link do seu app você verá o retorno de um JSON com as informações, deixe essa variável setada como <strong>false</strong> pois criaremos outra aplicação onde o retorno será <strong>true</strong>.
---
# Passo 7:

* ## Configurando Monitoração do PM2

* Acesse sua conta no site https://pm2.keymetrics.io/ e caso não possua, crie-a.
* Ao acessar sua conta voce verá um painel para criar um <strong>Bucket</strong>.
* Nomeie como quiser, e esse será nome do monitor de processos onde voce configurar as <strong>keys</strong>, as variáveis de ambiente relacionado à esse bucket.

* Ao criar seu <strong>Bucket</strong> lhe serão fornecidas duas senhas, uma <strong>PUBLIC_KEY</strong> e <strong>SECRET_KEY</strong>.
* Guarde com você essas informações, elas são <strong>sensíveis</strong>.

* Para setar essas variáveis, basta utilizar o comando realizando as devidas substituições.
* Copie todo o código, as contra-barras servem pra identificar uma quebra de linha no terminal

      heroku config:set \
       PM2_PUBLIC_KEY=CHAVE_PUBLICA \
       PM2_SECRET_KEY=CHAVE_PRIVADA \
       PM2_MACHINE_NAME=NOME_DO_SERVER \
       --app NOME_DO_APP_NO_HEROKU

* Com isso, atualize a página do Bucket no site do PM2 e você verá todas as informações em real time.

---
* ## Prontinho, sua aplicação já está pronta pra que você realize requisições no Front-End

---
# Passo 8:

* Vamos criar nossa <strong>segunda aplicação</strong> onde ela fornecerá as informações invertidas.
* Ao criar seu novo app, lembre-se que onde for necessário colocar o <strong>nome-do-seu-app</strong> será exatamente o nome desse novo app que você irá colocar a partir daqui.

* Para isso repita o processo dos <strong>Passos 1 e 2</strong>, com uma pequena alteração no <strong>Passo 2</strong>.
* Você irá renomer o remote do heroku para <strong>upside-down</strong>.

      git remote rename heroku upside-down

---
# Passo 9:

* Execute novamente os <strong>Passo 3 e 4</strong> lembrando de substituir no git push o <strong>hawkings</strong> por <strong>upside-down</strong>.

---
# Passo 10:

* Você pode pular o <strong>Passo 5</strong> pois já estará com o pm2 instalado globalmente, com isso vá para o <strong>Passo 6</strong> onde haverá agora a alteração do valor da variável de ambiente, o comando será:

      heroku config:set UP_DOWN=true --app nome-do-seu-app-aqui

---
# Passo 11:

* Execute o <strong>Passo 7</strong> para adicionar esse novo app ao seu monitor do PM2.
* Na linha do <strong>PM2_MACHINE_NAME</strong>, escolha outro nome pra que você visualize os 2 servidores

---
---
---
# Parabéns, você realizou 2 deploy's da mesma aplicação utilizando variáveis ambiente
