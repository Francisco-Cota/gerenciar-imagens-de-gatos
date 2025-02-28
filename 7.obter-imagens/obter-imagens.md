## Obter imagens

**Endpoint:** `GET /images`

Obtenha todas as imagens enviadas para sua conta via `/images/upload`. Os resultados podem ser filtrados através dos seguintes parâmetros `query`:

| Parâmetro |    Descrição      | Tipo | Obrigatório |
|------------|--------------------|------|------------|
| `limit`  | Número de resultados a serem retornados. O valor máximo é 25. O padrão é 1. | `integer` | Sim |
| `mime_types` | Os tipos de imagem a serem retornados: .gif, .jpg, ou .png. Retorna todos os tipos como padrão. | `string` delimitado por vírgulas. | Não |
| `order` | A ordem de retorno: RANDOM, ASC ou DESC. O padrão é RANDOM. | `string` | Não  |

Segue exemplo de chamada:

```json
curl --location 'https://api.thecatapi.com/v1/images?limit=100&order=ASC' \
--header 'x-api-key: live_2du7MqgVFkeexQfcCL0Vn738CK9AnmW1Ye20vPbZ35WFKv507Y3NAGQYnt7hIbOB'
```

A resposta de código `200 OK` indica que a obtenção da imagem foi executada com sucesso. E retorna um JSON com as informações da imagem recém-obtida. Por exemplo: 

```json
[
    {
        "breeds": [],
        "id": "3Ia--W4GM",
        "url": "https://cdn2.thecatapi.com/images/3Ia--W4GM.jpg",
        "width": 800,
        "height": 799,
        "sub_id": null,
        "created_at": "2024-10-18T01:22:05.000Z",
        "original_filename": "Cat03.jpg",
        "breed_ids": null
    },
    {
        "breeds": [],
        "id": "uDA8Z17di",
        "url": "https://cdn2.thecatapi.com/images/uDA8Z17di.jpg",
        "width": 275,
        "height": 183,
        "sub_id": null,
        "created_at": "2022-11-24T16:35:58.000Z",
        "original_filename": "index.jpg",
        "breed_ids": null
    },
    {
        "breeds": [],
        "id": "V1EFdLiCO",
        "url": "https://cdn2.thecatapi.com/images/V1EFdLiCO.png",
        "width": 860,
        "height": 733,
        "sub_id": null,
        "created_at": "2022-11-24T15:28:59.000Z",
        "original_filename": "41-415477_cat-tongue-png-cute-cat-png-transparent-png.png",
        "breed_ids": null
    }
]
```
