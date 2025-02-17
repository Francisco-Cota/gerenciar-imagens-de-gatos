## Deletar imagem

**Endpoint:** `DELETE /images/{image_id}`

Exclua a imagem correspondente ao parâmetro `image_id` passado como parâmetro `path`.

Segue exemplo de chamada:

```json
    curl --location --request DELETE 'https://api.thecatapi.com/v1/images/SAGEzuuKP' \
    --header 'x-api-key: live_2du7MqgVFkeexQfcCL0Vn738CK9AnmW1Ye20vPbZ35WFKv507Y3NAGQYnt7hIbOB'
```
A resposta de código `400 Bad request` indica que o apagamento da imagem foi executado com erro. Por exemplo:

    INVALID_DATA
