# Criar, Configurar e Conectar MongoDB à uma API

#### 5 min. de leitura | 12/09/2020 <br>

## O que é MongoDB
O MongoDB é um banco de dados NoSQL¹ bem prático e fácil de se utilizar. Decidi utilizá-lo pois a curva de aprendizado necessária para usar ele é pequena, já que meu foco atual é aprender como desenvolver uma API REST com Node.js.

Eu utilizei o [MongoDB Atlas](https://www.mongodb.com/) para a criação do meu banco. Logo após registrar uma conta e seguir os primeiros passos no site, o Cluster já estava sendo criado e iniciei as configurações de *Security*.
![](/mongodb/images/secao_security.png)

## Configurar *Database Access*
Para configurar o acesso à base de dados é necessário criar um usuário, na opção *Add New Database User*.

![](/mongodb/images/criar_usuario.png)
As demais configurações pode deixar como está na imagem. Após configurar, basta clicar no botão *Add User*.

Após a criação, a seção *Database Access* deve ter algo parecido com isso:

![](/mongodb/images/usuario_criado.png)
*OBS: Algumas configurações podem demorar para ficarem prontas, pois o servidor está na nuvem.*

## Configurar *Network Access*
Outra seção que deve ser configurada antes de usar o seu banco. Depois de entrar nela, basta clicar em *Add IP Address*. Após isso, é só selecionar a opção *Allow Access From Anywhere* e clicar em *Confirm*.

![](/mongodb/images/criar_acesso.png)
Depois de criar o acesso, o *Status* da conexão estará como *Pending*, aguarde até ficar *Active*.

## Conectar a API ao banco com Mongoose
O Mongoose é um ODM² feito para facilitar o uso do MongoDB no Node.js. Com ele, se torna muito simples configurar a conexão com o banco de dados.

Eu pensava que era complicado de conectar, mas na realidade foi bem simples. Basta ir no seu Cluster e selecionar a opção de connect. Posteriormente, foi só selecionar o driver do Node.js e copiar a URL como está exemplificado na imagem:

![](/mongodb/images/conexao_cluster.png)


Após isso, foi só configurar o servidor em um arquivo (server.js) e pronto, já estou conectado.

Exemplo de conexão:
```js
const mongoose = require('mongoose')

mongoose.connect('mongodb+srv://<user>:<password>@cluster0.rkx57.mongodb.net/<dbname>?retryWrites=true&w=majority', { 
    useNewUrlParser: true,
    useUnifiedTopology: true
})
```
**OBS:** É necessário substituir as tags *user*, *password* e *dbname* pelas configuradas no MongoDB Atlas.

<hr>

NoSQL¹ - Termo genérico usado para representar bancos de dados não relacionais, como MongoDB e o Couchbase. Diferentemente dos bancos SQL, bancos não relacionais podem ser bem diferentes entre si;

ODM² - É um acrônimo para *Object Data Model*, que é um modelo de data (uma maneira de escrever comandos para o banco) baseado em programação orientada à objetos.

Posteriormente estarei disponibilizando um link de um vídeo que farei de um CRUD com Node.js, Express e MongoDB. Lá, farei passo a passo o que foi escrito aqui.