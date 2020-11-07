# Rest e Spread

São dois conceitos similares que podem ajudar muito na programação. Descobri a importância desses operadores ao precisar reduzir meu código em PHP, porém lembrei da existência deles em JavaScript e resolvi praticar um pouco.

Segue um exemplo:
```js
// REST

const duplaA = ['Juliano', 'Éderson']
const duplaB = ['Huriel', 'Marcelo']

const duplas = [...duplaA, ...duplaB, 'Gregori', 'Felipe' ]

console.log(duplas)

// Resultado:
// ["Juliano", "Éderson", "Huriel", "Marcelo", "Gregori", "Felipe"]
```
O resultado do *console.log* será um array só contendo todas os valores juntos. Isso ocorre pois o `rest` permite passar quantos valores quiser em forma de um *array*. Caso as variáveis fossem passadas sem os `...` o resultado seria diferente, tendo *arrays* dentro de *arrays* .

Já o `spread`, fará uma funcionalidade diferente, confira:
```js 
// SPREAD

function linguagens(lingPrincipal, ...lingsSecundarias) {
    console.log(lingPrincipal, lingsSecundarias)
}

linguagens('JavaScript', 'CSS', 'HTML', 'Markdown')

// Resultado:
// "JavaScript" ["CSS", "HTML", "Markdown"]
```
Nesse *console.log*, aconteceria o oposto, pois ele uniu todos os parâmetros passados - com exceção do primeiro - em um *array*, exibindo os demais no *console.log* entre [], sendo que foram passados como strings.

Para conferir esses códigos funcionando, [clique aqui](https://codepen.io/huri3l/pen/wvGJXoV) - *É necessário clicar em console, no canto inferior esquerdo da página.*
