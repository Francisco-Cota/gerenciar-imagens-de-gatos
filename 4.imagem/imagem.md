## Imagem
O objeto `images`representa as fotos de gatos enviadas.

> Imagens que não contiverem gatos ou forem inapropriadas são  
> rejeitadas.

| Nome | Descrição | Tipo | Obrigatório |
| --- | --- | --- | --- |
| `id` | ID da imagem. | `UUID` | Sim |
| `url` | URL para acessar a imagem. | `string` | Sim |
| `width` | Largura da imagem em pixels. Automaticamente gerada. | `integer` | Sim |
| `height` | Altura da imagem em pixels. Automaticamente gerada. | `integer` | Sim |
| `sub_id` | ID para identificação interna. | `string` | Não |
| `created_at` | Data de upload da imagem no formato _2022-11-24T17:41:35.000Z_ | `datetime` | Sim |
| `original_filename` | Nome do arquivo original. | `string` | Sim |
| `pending` | Flag interna de ciclo de vida. 0=falso, 1=verdadeiro | `integer` | Não |
| `approved` | Flag interna de ciclo de vida. 0=falso, 1=verdadeiro | `integer` | Não |
| `breed_ids` | **Não implementado.** | N/A | Não | 