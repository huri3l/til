# Arquivos Específicos Para Commit

Com o Git, é possível utilizar certos parâmetros no ```git add``` para executar tarefas em grupo.

### Adicionar apenas arquivos modificados e deletados:
```git
git add -u 
```
A *flag* -u é um atalho para --update, sendo assim, adiciona ao commit apenas os arquivos modificados e deletados.

### Adicionar apenas arquivos novos:
```git
git add $(git ls-files -o --exclude-standard)
```
O ```git ls-files``` mostra uma lista de arquivos, e quando usa-se a *flag* ```-o``` o filtro inclui apenas os arquivos mostrados no *others* (*untracked files*, que seriam os arquivos que aparece em *others* no ```git status```, ou seja, apenas os novos arquivos). O ```$(...)``` é passado como parâmetro ao ```git add``, e o que está dentro dele retornou apenas os arquivos recém colocados.
