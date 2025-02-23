## Obter imagem por ID

**Endpoint:** `GET /images/{image_id}`

Obtenha a imagem correspondente ao parâmetro `image_id` passado como parâmetro `path`. Segue exemplo de chamada:

        curl --location 'https://api.thecatapi.com/v1/images/SAGEzuuKP' \
        --header 'x-api-key: live_2du7MqgVFkeexQfcCL0Vn738CK9AnmW1Ye20vPbZ35WFKv507Y3NAGQYnt7hIbOB'
    

Neste exemplo, o parâmetro `image_id` é o mesmo encontrado no passo anterior: `GET /images/SAGEzuuKP`.

A resposta de código `200 OK` indica que a obtenção da imagem foi executada com sucesso. E retorna um JSON com as informações da imagem recém-obtida. Por exemplo:

    {"id":"SAGEzuuKP","url":"https://cdn2.thecatapi.com/images/SAGEzuuKP.jpg","width":1280,"height":960}
    

A resposta de código `400 Bad request` indica que a obtenção da imagem foi executada com erro. Por exemplo:

    Couldn't find an image matching the passed 'id' of {{image_id}}
    

> Para se recuperar do estado de erro, insira o ID da imagem diretamente no path, no parâmetro `{{image_id}}`.
