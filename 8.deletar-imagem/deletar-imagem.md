## Deletar imagem

**Endpoint:** `DELETE /images/{image_id}`

Exclua a imagem correspondente ao parâmetro `image_id` passado como parâmetro `path`.

Exemplo de chamada:

        curl --location --request DELETE 'https://api.thecatapi.com/v1/images/SAGEzuuKP' \
        --header 'x-api-key: live_2du7MqgVFkeexQfcCL0Vn738CK9AnmW1Ye20vPbZ35WFKv507Y3NAGQYnt7hIbOB'
    

A resposta de código `204 No content`indica que a imagem foi excluída com sucesso e o sistema não retorna um JSON nesse caso.

Para conferir a exclusão, chame `GET /images/{image_id}` com o `image_id` da imagem excluída.

A resposta de código `400 Bad request` indica que a exclusão da imagem foi executada com erro. Por exemplo:

    INVALID_DATA
