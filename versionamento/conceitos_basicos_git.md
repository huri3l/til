# Conceitos Básicos de Git

Recentemente entrei em uma jornada para aprender a usar terminais (eu meio que tinha medo hehe). Nesse contexto, estou passando por uma período de substituição do GitHub Desktop para utilizar apenas linhas de comando.

## O que é Git
Git é um sistema de versionamento, através do qual se torna possível manter um controle das versões de um software (por exemplo), e assim, navegar entre elas. É possível que duas pessoas tenham versões diferentes de um mesmo projeto e depois uni-las em um resultado final só. Além disso, o Git oferece outras possibilidades, como usar versões antigas dos projetos com segurança e facilidade.

## O que é Branch
Branch é basicamente um "mini-projeto" dentro do seu projeto Git através do qual você pode fazer alterações sem mexer com a master (a versão original do projeto), enviando para ela apenas os branchs devidamente testados e configurados.

## O que é Merge
Merge é a ação de juntar o código de um branch com a master.

## Comandos básicos
Logo após a instalação do [Git](https://git-scm.com/downloads/), é importante configurar um "usuário", da seguinte forma:

```git
git config --global user.name "Seu Nome"
git config --global user.email "seu@email.com"
```

Esse "usuário" será usado para registrar quais *commits* foram feitos por você no projeto, dessa forma:

```git
commit 4b858fdfa370bdd6e825431410a5889929d292a6 (HEAD -> master)
Author: Huriel Lopes <huriel@exemplo.com>
Date:   Thu Nov 5 23:33:12 2020 -0300
```

Viu como o nome e o e-mail apareceram ali? Já já mostro como fazer isso, temos outras coisas pra configurar antes.

Agora, vamos iniciar um projeto. Para isso, basta selecionar uma pasta onde deseja iniciar e usar o comando:

```git
git init
```

Pronto, criado :D

Após criar um projeto, há alguns comandos importantes que vou passar abaixo e suas respectivas funções:

* **git status** - Verifica o status do projeto e nos retorna o que tá acontecendo;

* **git add** - Adiciona um novo arquivo, um arquivo deletado ou editado ao *commit*;

* **git commit** - Realiza o *commit*;

* **git log** - Mostra o registro de commits realizados;

* **git branch (nome do branch)** - Cria um *branch*;

* **git checkout (nome do branch)** - Troca de *branch*;

* **git checkout -b (nome do branch)** - Cria um *branch* (uma área de trabalho "longe" da *master*) e já troca para trabalhar nele;

* **git merge (nome do branch)** - Realiza o merge do *branch* na *master* (é necessário estar na master, e para isso, use o git checkout)