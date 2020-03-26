# Feed de Produtos

Os dados do produto são o coração do ciclo de vida do PowerReviews UGC. Ter informações atuais e atualizadas sobre o produto é fundamental para garantir que serviços como Avaliações e Revisões, Coleta de E-mail, Sindicância e outros tenham todos os dados necessários para funcionar plenamente. Existem duas maneiras de fornecer ao powerreviews suas informações de produto: através de um feed ou usando Feedless. Este documento irá guiá-lo durante o processo de uso de um feed de produto. Para configurar o Feedless, consulte a documentação feedless.

O PowerReviews pode aceitar o feed do produto nos seguintes formatos:

* Google Merchant Product Feed (TXT or XML)
* UTF-8, no BOM (TXT or CSV)

**Feed de Produtos Google Merchant**

Muitos clientes do PowerReviews já estão fornecendo um Feed de Produto Do Google Merchant para o Google. Se você estiver gerando este arquivo, pode ser possível usar sua alimentação existente com alguns requisitos adicionais. Se você deseja tentar usar um Feed de Produto Do Google Merchant existente, você pode encontrar mais informações no [Google Merchant Product Feed]().

**Campos Necessários**

Os campos listados na tabela abaixo são necessários para cada importação do feed de produto PowerReviews. Combine a ortografia exata e a capitalização para garantir que seu código seja preciso.

|Campo|Exemplo|Descrição|Tamanho|Notas Adicionais|
|-----|-------|---------|-------|----------------|
|page_id|xlslmpprod1790001|O identificador único do produto; Tipicamente o produto, id, SKU, style number, item number ou código UPC. Este campo é case-sensitive e não deve incluir espaços.|Até 50 caracteres|Este campo também é usado pelo feed de pedido do Collect Email.|
|product_url|https://www.nike.com.br/Produto/Tenis-Nike-Air-Max-Verona-Feminino/1-16-213-207448|A URL da página de detalhes do produto em seu site. Se você participar de PLAs do Google, forneça URLs canônicos ou considere enviar PowerReviews ao seu Feed de Produto Comercial do Google.|Até 650 caracteres|Este campo não deve conter espaços.|
|name|Nike Air Max Verona|O nome do produto|Até 500 caracteres|Codificar todos os caracteres especiais.|
|image_url|https://images.lojanike.com.br/500x500/produto/207439_1964518_20200218152005.jpg|a URL da imagem do produto. Certifique-se de usar uma imagem de alta qualidade. É melhor não usar caracteres especiais na URL e nome da sua imagem sem que a URL codifique o nome.|Até 650 caracteres|A imagem deve ter pelo menos 350 pixels em uma dimensão.|
|description|Em 1992, a Nike lançou o Air Verona: o primeiro tênis de corrida com Air exclusivo para elas. Hoje, quase 30 anos depois, o Air Max Verona traz um solado elevado e uma bolha mega confortável que além de combinar com o seu look é o tênis ideal para o seu dia a dia.|Uma longa descrição do produto. A marcação HTML não deve ser incluída na descrição.|Até 10,000 caracteres|Você deve escapar de todas as aspas duplas. Se seus dados contêm caracteres especiais, certifique-se de envolver todo o valor entre aspas. Não inclua HTML ou quebras de linha.|
|category|Feminino>Calçados>Casual|A classificação do produto no inventário. Para indicar uma hierarquia, use o símbolo maior que (>) como um delimitador entre categorias, semelhante ao exemplo. Dependendo do modelo de navegação do seu site, a classificação de inventário pode corresponder às categorias de navegação.|Até 300 caracteres| |
|brand|Nike|A marca do produto. Este valor deve corresponder com precisão ao nome da marca dado em seu site.|Até 50 caracteres|Este campo é necessário se você participar do Syndication.|
|upc|872760558488 (upc) or 0872760558488 (ean)|O código de 12 dígitos universal do produto ou o número Artigo internacional de 13 dígitos. Se você participa no Google PLAs, este campo é necessário. Você também pode enviar ao PowerReviews seu feed de produto do google merchant.|Deve ter 12 ou 13 caracteres numéricos|Este campo é necessário se você participar do Syndication.|
|manufacturer_id|xlslmpprod-1790001-a|O número do modelo do fabricante|Sem limite|Este campo é necessário se você participar do Syndication.|

> :warning: Você deve escapar de todas as aspas duplas no campo de descrição. Se seus dados contêm caracteres especiais, certifique-se de envolver todo o valor entre aspas. Para obter as melhores práticas na formatação de seus dados para consumo pelo PowerReviews, consulte [este documento](this-doc.md).

**Campos opcionais**

Os campos listados na tabela abaixo são opcionais para cada importação do feed de produto PowerReviews. Se você optar por usá-los, use os nomes de campo exatamente como eles estão fornecidos na tabela abaixo.

|Campo|Exemplo|Descrição|Tamanho|
|-----|-------|---------|-------|
|page_id_variant|1234_blue|A variante do produto. Este campo é usando primariamente quando o **page_id** tem múltiplos variantes de item-nível. Para mais informações sobre como incluir variantes em seu feed de produto, consulte: [Ids de página e Variantes]()|Até 50 caracteres|
|add_to_cart_url|https://www.example.com/store/cart-AddProduct?pid=1234&Quantity=1|O hiperlink para adicionar o produto ao carrinho do cliente.|Até 650 caracteres|
|in_stock|1|A indica o status do produto no estoque. O valor 0 indica não, e o valor 1 indica sim.|1 caractere|
|price|599.99|O preço de venda atual do item. A formatação cambial internacional não é suportada. Inclua o ponto decimal no preço, mas não inclua nenhum sinal de dólar ou vírgulas.|Até 650 caracteres|

Para criar o feed de produto:

1. Baixe um formato de arquivo de exemplo, pode ser formato TXT ou CSV. Você deve formatar este arquivo com codificação UTF-8 e sem BYTE ORDER MARK (BOM).
2. Edite o arquivo de exemplo que você baixou usando os nomes dos campos PowerReviews como títulos das colunas.
3. Carregue seu arquivo para seu próprio SFTP, o SFTP fornecido pelo PowerReviews ou forneça uma URL pública. Se você optar por usar seu próprio SFTP, forneça ao PowerReviews o local e credenciais necessários para acessar o arquivo. Se você deseja usar um SFTP fornecido pelo PowerReviews e não tiver suas credenciais, entre em contato para solicitá-las.
4. Certifique-se de que o nome do arquivo e o local estão estáticos.
Quando configuramos a importação de feed do produto no back-end, ele depende de procurar o mesmo arquivo todas as vezes. Se você precisar renomear seu feed ou movê-lo para outro local, você precisará entrar em contato conosco quando isso ocorrer para que possamos atualizar a configuração para você.
5. Depois de concluir as etapas anteriores, entre em contato com os Serviços Técnicos do PowerReviews para solicitar que configuremos seu feed para importação em nossos sistemas.

Recomendamos que você automatize esse processo no seu final, para garantir que sempre que as informações do seu produto forem alterados, receberemos esses dados em um arquivo de feed atualizado automaticamente. Caso contrário, será importante certificar-se de que o arquivo é atualizado manualmente e colocado no local onde estamos procurando por ele em uma base recorrente.

## Processando o Feed de Produto

Os feeds do produto são normalmente processados a cada 48 horas. Se você carregar uma novo feed do produto, por favor, permita que este tempo seja importado para o nosso sistema. Se após esse tempo você não ver suas atualizações para os dados do seu produto, entre em contato com os Serviços Técnicos para que possamos garantir que isso ocorreu.

## Perguntas Frequentes

**Por que não consigo me conectar à conta FTP/SFTP?**
Se você está tentando se conectar a partners.powerreviews.com, observe que este servidor não está mais em uso e o nome de host correto agora é: sftp.powerreviews.com. Nenhum _whitelist_ de IP é necessária para este servidor, porém ele só suporta SFTP e FTPS. FTP não é mais suportado. Se você ainda tiver dificuldade em se conectar depois de garantir que está tentando se conectar ao servidor correto com um protocolo suportado, entre em contato com os Serviços Técnicos do PowerReviews.

**Precisamos adicionar o servidor SFTP do PowerReviews ao whitelist. Como fazemos isso?**
Dado o comportamento intrínseco da rede em nuvem, é possível que nossos endereços IP de saída possam mudar sem aviso prévio. Recomendamos que você evite usar os IPs específicos e, em vez disso, detectá-los dinamicamente usando os 3 CNAMEs que mapeiam para os gateways NAT que usamos:

prod-nat1.powerreviews.com

prod-nat2.powerreviews.com

prod-nat3.powerreviews.com

**Por que não há imagens/nomes para produtos com moderação ou no formulário 'Write A Review'?**
Os nomes e imagens dos produtos são provenientes dos dados do produto que você nos fornece. Se você estiver usando nossa solução de catálogo sem feed, o nome e a URL da imagem são necessários. Se você estiver nos enviando um feed de produto, certifique-se de que nomes e imagens de produtos sejam fornecidos para todos os produtos. Para garantir que o arquivo seja capaz de ser importado do nosso lado, certifique-se de que você está codificando caracteres especiais usando a codificação HTML padrão. Além disso, certifique-se de envolver qualquer campo que contenha vírgulas com aspas duplas (não codificadas, porém - esta é a única vez que isso não é necessário). Por último, certifique-se de que todas as linhas contêm a mesma quantidade de campos que há cabeçalhos de coluna.

**Quais são as vantagens de usar variantes versus apenas ter um ID de página diferente para cada produto?**
As variantes lhe dão a capacidade de mostrar informações diferentes no formulário Write-A-Review enquanto exibem as avaliações em conjunto. As variantes também facilitam as migrações de revisão (ou seja, se certas revisões ligadas a variantes específicas precisarem ser movidas). Além disso, se você estiver participando do Syndication, as variantes podem ser necessárias para garantir que estamos recebendo todos os UPCs disponíveis para um produto para que a correspondência possa ocorrer. Para obter mais informações, consulte: [IDs de página e variantes](page-id-and-variants.md).