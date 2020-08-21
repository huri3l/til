# A importância do package.json

#### 6 min. de leitura | 19/08/2020 <br>

Ao iniciar meus estudos em cima do `Node`¹ e das novidades apresentadas a partir do `ES6+`², me deparei com um arquivo chamado `package.json`. Logo de cara, pude ver qual era sua função, porém fui ainda mais a fundo para entender o que era possível fazer com ele.

**O arquivo em formato `JSON`³ possibilita guardar várias informações distintas sobre o seu projeto,** como o nome, a versão e as dependências do mesmo. Segue abaixo um exemplo:

```json
{
  "name": "aplicacao-exemplo",
  "version": "1.0.0",
  "description": "Uma aplicação de exemplo para package.json",
  "dependencies": {
    "vue": "^2.5.2"
  },
  "devDependencies": {
    "@babel/cli": "^7.10.5",
    "@babel/core": "^7.11.1",
    "@babel/plugin-proposal-object-rest-spread": "^7.11.0",
    "@babel/preset-env": "^7.11.0"
  },
  "scripts": {
    "dev": "babel ./main.js -o bundle.js -w"
  }
```
Compreendi que esse arquivo é deveras importante para o profissionalismo do projeto. Nele é possível manter tudo organizado e resumido em um só lugar!

Mas bem, não se sinta perdido. Vamos às explicações.

* "name": Este é o nome do seu projeto, do que está sendo desenvolvido;
* "version": É a versão do mesmo;
* "description": Uma breve descrição sobre o que essa aplicação é;
* "dependencies": Um objeto que inclui as dependências de sua aplicação. No caso, o que ela precisa para funcionar;
* "devDependencies": Tem o mesmo intuito que o item anterior, entretanto, são apenas dependências para desenvolvimento. Enquanto se desenvolve o projeto, é necessário ter o que está mencionado dentro desse objeto, porém não é necessário para que a aplicação funcione;
* "scripts": São atalhos para executar uma linha de código de maneira rápida. Nesse cenário, é possivel escrever apenas o nome do script, e não a linha inteira.

Essas são as principais funções desse arquivo, ainda há várias outras que podem ser utilizadas. Para conferir ainda mais conteúdo sobre esse assunto, estarei disponibilizando alguns links extras:

[Especificações do tratamento de package.json](https://docs.npmjs.com/files/package.json) - Uma lista do que pode ser usado no package.json *(A leitura é nativamente em inglês)*.

[Tudo que você queria saber sobre o package-lock.json mas estava com vergonha de perguntar](https://medium.com/trainingcenter/tudo-que-você-queria-saber-sobre-o-package-lock-json-mas-estava-com-vergonha-de-perguntar-e70589f2855f) - Uma leitura a respeito do arquivo `package-lock.json`, que tem uma conexão com o assunto desse artigo.

<hr>

Node¹ - Runtime de JavaScript que possibilita a utilização dessa linguagem no backend;

ES6+² - ECMAScript. Seria o padrão da linguagem JavaScript. ES6+ se refere às grandes mudanças que houveram a partir da versão 6, lançada em 2015.

JSON³ - JavaScript Object Notation. É um formato compacto de objeto utilizado para a troca de dados de forma rápida e simples entre os sistemas.
