# Códigos de Status HTTP
## Descrição sobre Diversos Códigos de Status nas Requisições HTTP

### Códigos de Status:

### 1. Respostas Bem-Sucedidas (200 - 299)
#### 200: Ok
#### Sua solicitação foi bem-sucedida e o servidor deve responder de acordo com o protocolo http
#### utilizado, tais como:

1. `GET`: O recurso da requisição foi obtido com sucesso e está presente no corpo da resposta. Esse código é comum em operações de leitura ou consultas de dados.
2. `DELETE`: A requisição para excluir um recurso foi aceita e concluída com sucesso. O recurso foi removido permanentemente, se existente.
3. `PUT`: Indica que a requisição para atualizar uma informação ou recurso ocorreu com êxito, o servidor normalmente da um retorno de bem sucedido para a operação.
4. `POST`: Indica que a requisição para criar um novo recurso foi bem-sucedida. O Servidor retorna este status code após ter criado com sucesso as modificações requeridas pelo cliente.
5. `PATCH`: A modificação parcial do recurso foi realizada com sucesso. O servidor aplicou apenas as alterações especificadas.

#### 201: Created
 Esse status code sinaliza que a solicitação do cliente foi aceita pelo servidor e o mesmo resultou 
 na criação de um ou mais novos recursos. O recurso principal criado pela solicitação é identificado 
 por um campo de cabeçalho *Location* na resposta ou, se nenhum campoo de cabeçanho *Location* for
 recebido, pelo URL de destino.


#### 202: Accepted
O recusor foi aceito, embora seu conteúdo ainda não tenha sido processado. Trata-se de uma resposta que o servidor envia como forma de validar que o recurso foi recebido, mas não finalizada, uma resposta evasiva por parte do servidor, algo como "Recebi o seu pedido, mas o relatório ainda não está pronto". O servidor aceitou a requisição do usuário, mas seu processamento pode demorar por ser algo assíncrono (ou seja, o servidor não bloqueia o cliente aguardando a conclusão).

#### 203: Non-Authoritative Information
O status code 203 (Non-Authoritative Information) indica que a requisição foi bem-sucedida, mas a resposta recebida pelo cliente *não é exatamente a mesma* enviada pelo servidor de origem — ela foi modificada por um intermediário (como um proxy ou CDN). Por exemplo: um proxy pode comprimir uma imagem ou filtrar dados sensíveis antes de repassar a resposta, e o 203 avisa que essa versão não é 'oficial', mas ainda assim válida. O seu uso é raro e mesmo certos proxies retornam 200 *OK*

#### 204: Not Content
Aqui o servidor recebeu a requisição do cliente e a mesma foi bem-sucedida, embora não haja nada para retornar no campo da resposta.
- ela é útil em um *DELETE* bem-sucedido, onde o recurso foi removido e não há mais nada para dizer.
- Também em casos de *PUT* e *POST* qua atualizou um recuso, mas não precisa enviar confirmação.
  
#### 205: Reset Content 
Aqui o servidor responde: "Sua requisição foi bem-sucedida, mas o cliente deve *reiniciar a visualização atual (como um formulário ou documento).*".
- Depois de um *POST* (comu um formulário de login), o servidor pode responder com 205 para indicar que o navegador deve *limpar os campos* (evitando reenvio acidental).
- Se uma ação requer que o cliente volte ao estado inicial (ex: um editor de texto após salvar), o 205 pode ser usado para disparar essa limpeza.

#### 206: Conteúdo parcial
#### 207: Status Multi (Especifíco do WebDAV, não oficial)
