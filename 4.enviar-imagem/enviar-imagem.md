## Enviar imagem

**Endpoint:** `POST /images/upload`

Cria uma nova imagem no sistema carregando um arquivo .gif, .jpg, ou .png válido contendo um gato.

**Request body**

| Nome | Descrição | Tipo | Obrigatório |
|------|-----------|------|-------------|
| `file` | Arquivo em .gif, .png, ou .jpg | `file` | Sim |
| `sub_id` | Alt text para identificação interna. | `string` | Não |

**POST**

Para enviar uma imagem, chame:  
`POST /https://api.thecatapi.com/v1/images/`, com o corpo da requisição contendo as informações da imagem. Por exemplo:

    curl --location 'https://api.thecatapi.com/v1/images/' \
    --header 'x-api-key: live_2h44mkM5Nbi4ShwKRgvV21TMDbqfFp3h9NE85WpJYJsFT9kyNrLHRDypRJIHTXjA' \
    --form 'file=@"WPDxeUKo1/kitten-227011_1280.jpg"' \
    --form 'sub_id="Imagem de um gato branco filhote em uma toalha rosa"'
    

> Observação: Se já houver um `ID`da imagem para identificação interna, preencha o corpo da requisição com o `sub_id` do tipo string.

A resposta de código `200 OK` indica que o envio da imagem foi executado com sucesso. E retorna um JSON com as informações da imagem enviada, incluindo sua URL. Por exemplo:

    {
        "id": "SAGEzuuKP",
        "url": "https://cdn2.thecatapi.com/images/SAGEzuuKP.jpg",
        "sub_id": "Imagem de um gato branco filhote em uma toalha rosa",
        "width": 1280,
        "height": 960,
        "original_filename": "kitten-227011_1280.jpg",
        "pending": 0,
        "approved": 1
    }
    

Imagem exemplo:  
![Imagem de um gato branco filhote deitado em uma toalha rosa.](https://cdn2.thecatapi.com/images/SAGEzuuKP.jpg)

> Imagem de um gato branco filhote deitado em uma toalha rosa.

A resposta de código `400 Bad request`indica que o envio da imagem foi executado com erro. Por exemplo:

    No 'file' sent. Check you're sending the image as the 'file' parameter. of the FormData object.
    

> Para se recuperar do estado de erro, confira se você está enviando a imagem como o parâmetro `file`.