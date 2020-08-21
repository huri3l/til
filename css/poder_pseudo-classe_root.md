# O Poder da Pseudo-Classe Root

#### 19/08/2020 | 3 min. de leitura <br>

Vasculhando um pouco sobre variáveis no CSS, descobri que a pseudo-classe `:root` serve para mais coisas do que eu imaginava. No raso conhecimento que tinha, imaginei que servisse somente para declarar variáveis, então fui mais a fundo. <br>
Devido ao significado de `root` (raíz), essa pseudo-classe tem o poder de mexer com todos os elementos da tela, já que é a **raíz da árvore de elementos distribuídos pela página**. <br>
Tendo isso em mente, é possível fazer estilizações como essa:
```css 
    :root {
        /* Boa e velha declaração de variável */
        --variable-a: value;

        /* Alteração de fonte e cor  */
        font-family: Arial;
        color: green;
    }
```
Tal alteração irá fazer com que todos os elementos de texto da página tenham fonte Arial e cor verde. É uma infinidade de possibilidades! Isso com certeza irá aumentar minha produtividade e espero que ajude a sua também. <br>
*Observação: a tag do elemento é indiferente, (p, h1, a...), sendo texto, a alteração será aplicada.* <br>
Para conferir um exemplo, [clique aqui](https://codepen.io/huri3l/pen/WNwGgvV).
