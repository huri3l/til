# Desestruturação: o poder da produtividade

As possibilidades que o ES6+ trouxe para o JavaScript me surpreendem mais a cada dia! Estava estudando sobre, pois, um passarinho me contou que muitas coisas adicionadas facilitam muito na produtividade e também deixam o código limpo. Como passarinhos são duvidosos, fui pesquisar a respeito e pratiquei um pouco de *destructuring assignment*.

A desestruturação é uma maneira alternativa à convencional usada para obter dados de objetos e vetores (arrays) e colocá-los em variáveis, de forma rápida e com um código mais enxuto. Segue um exemplo:
```js
    var aluno = {nome: 'Huriel', curso: 'Ciências da Computação', idade: 18}
    
    // Método convencional:
    var nome = aluno.nome
    var curso = aluno.curso
    var idade = aluno.idade

    // Destructuring Assignment
    let { nome, curso, idade } = aluno
```

Tanto o método convencional quanto a desestruturação, estão fazendo exatamente a mesma coisa! Acontece que, com essa funcionalidade, o código fica muito mais amigável e organizado, além de possibilitarem o uso das variáveis de maneira equivalente!

Junto com a desestruturação, existe o `rest` e o `spread`, mas estarei abordando-os no próximo artigo, pois o objetivo desses é de proporcionar uma leitura rápida, então irei separá-los.

Para quem deseja uma leitura mais aprofundada no assunto, confira o link abaixo:

[Atribuição via desestruturação (destructuring assignment)](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Operators/Atribuicao_via_desestruturacao) - MDN Web Docs, fonte de grande parte deste artigo.