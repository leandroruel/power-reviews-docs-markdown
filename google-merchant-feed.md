# Feed de produto Google Merchant
O PowerReviews também aceita o formato de Feed de Produtos do Google Merchant, com alguns requisitos adicionais. Para obter mais informações sobre os feeds de produtos do Google Merchant, consulte o [Google Merchant Center Help](https://www.google.com/retail/solutions/merchant-center/).

As seções a seguir descrevem os pontos de dados e os requisitos adicionais do PowerReviews.

|Campo|Exigido por Google?|Requerimentos Adicionais|
|-----|-------------------|------------------------|
|id|Sim| |
|link|Sim|PowerReviews só podem ingerir os primeiros 650 caracteres ou menos. Este campo não deve conter espaços.|
|title|Sim| |
|image_link|Sim|PowerReviews só podem ingerir os primeiros 650 caracteres ou menos. A imagem deve ter pelo menos 350 pixels em uma dimensão.|
|description|Sim| |
|product_type OU google_product_category|Sim|Se você incluir ambos os valores, o PowerReviews só usará product_type. PowerReviews podem ingerir os primeiros 300 caracteres para este campo.|
|brand|Nem sempre|Este campo é necessário se você participar do Syndication.|
|gtin|Nem sempre|Este campo deve ter apenas 12 ou 13 dígitos. Este campo é necessário se você participar do Syndication.|
|mpn|Não|Este campo é necessário se você participar do Syndication.|

## Campos opcionais

Os campos listados na tabela abaixo são opcionais para cada importação de feed de produto PowerReviews. Se você optar por usá-los, use os nomes de campo exatamente como eles estão fornecidos na tabela abaixo.

|Campo|Exigido por Google?|Requerimentos Adicionais|
|-----|-------------------|------------------------|
|item_group_id|Não|	Isso é necessário se você usar Variantes.|
|availability|Sim| |
|price|Sim| |

Para incluir as variantes de ID de página, inclua o campo item_group_id. Ao usar variantes, o campo item_group_id é o seu exclusivo page_id(product_id) e o campo de identificação é a variante desse produto.
