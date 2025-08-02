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
O status code 203 (Non-Authoritative Information) indica que a requisição foi bem-sucedida, mas a resposta recebida pelo cliente não é exatamente a mesma enviada pelo servidor de origem — ela foi modificada por um intermediário (como um proxy ou CDN). Por exemplo: um proxy pode comprimir uma imagem ou filtrar dados sensíveis antes de repassar a resposta, e o 203 avisa que essa versão não é 'oficial', mas ainda assim válida.

#### 204: Sem conteúdo
#### 205: Reset / Redefinir conteúdo
#### 206: Conteúdo parcial
#### 207: Status Multi (Especifíco do WebDAV, não oficial)
