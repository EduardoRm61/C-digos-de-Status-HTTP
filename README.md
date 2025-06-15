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
