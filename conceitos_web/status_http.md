# Status HTTP

#### 3 min. de leitura | 12/09/2020 <br>

Os códigos de status HTTP informam se uma requisição foi corretamente concluída. As respostas são inclusas em grupos, sendo eles:

* **100-199** (Informação) - Solicitação aceita ou processo em andamento;
* **200-299** (Sucesso) - A ação foi concluída com êxito;
* **300-399** (Redirecionamento) - É necessário fazer mais coisas para completar a solicitação;
* **400-499** (Erros do cliente) - A requisição não pôde ser concluída;
* **500-599** (Erros do servidor) - O servidor falhou ao concluir a solicitação.

É deveras importante organizar e enviar o status correto na resposta da requisição do cliente pois isso, além de estar de acordo com os padrões da web, deixa o código semanticamente melhor.

Segue um exemplo de como abordei a resposta de status em um CRUD básico que estou desenvolvendo com Node e Express (tem um pouco de Mongoose aí também):
```js
    // O servidor não pode encontrar o usuário 
    // (404: Not found)
    if(!user) {
        return res.status(404).json({ error: 'Usuário não encontrado' })
    }
    
    // O servidor não pode encontrar a nota 
    // (404: Not found)
    if(!note) {
        return res.status(404).json({ error: 'Nota não encontrada' })
    }

    // O usuário atual não tem autorização para alterar a nota de outro usuário 
    // (403: Forbidden)
    if(!note.user_id.equals(user._id)) {
        return res.status(403).json({ error: 'Acesso negado' })
    }
```
Essas são algumas validações básicas que fiz na minha aplicação para melhorar o funcionamento dela e tratar certos erros de maneira simples.

Leitura complementar:

[Códigos de status de respostas HTTP](https://developer.mozilla.org/pt-BR/docs/Web/HTTP/Status) - Lista com os códigos de status HTTP. *Mozilla Developer Network*.