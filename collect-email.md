![logo](img/PR_logo.png)

# Coletar Email

Configurar um e-mail de pós-compra é essencial para obter mais avaliações adicionados aos produtos em seu site.

Usando **Collect Email** (Coletar Email), você pode enviar e-mails de acompanhamento aos seus clientes após a compra de um produto, convidando-os a escrever uma avaliação. Estudos mostram que até 60-80% das avaliações de clientes são resultado de solicitações por email.

Esta página contém as seguintes seções:
* [Pré-requisitos](#pre-requisitos)

* [Configurando Collect Email](#configurando-collect-email)

  * [Usando PowerReviews como seu Provedor de E-mails](#usando-power-reviews-como-seu-ep)

* [Agendando seus e-mails](#agendando-emails)

#### Pré-requisitos {#pre-requisitos}

Para implementar com êxito o Collect Email, verifique se você atendeu aos seguintes pré-requisitos:

* Ative o programa de e-mail PowerReviews. Para obter mais informações sobre como fazer isso, entre em contato com a equipe de implementação ou o diretor de sucesso do cliente, se você estiver fora de implementação.
* A coleta de email é direcionada pelos dados do pedido. Leia mais sobre como o PowerReviews pode ingerir os dados do seu pedido para decidir a melhor opção para o seu programa. Consulte [Opções e considerações dos dados do pedido]() para obter detalhes.
* Verifique se a página Write-A-Review (Escreva uma Avaliação) está definida e configurada corretamente. Você deve fornecer o URL Write-A-Review para o PowerReviews quando optar por usar o Collect Email.

> :warning: Se essa URL mudar, você deverá notificar o PowerReviews para atualizar as configurações da sua conta.

Também é importante observar que quando você configura seu Collect Email, o texto no email não é traduzido automaticamente para outros idiomas. A mensagem padrão para outros idiomas também não será traduzida automaticamente. Você deve preencher a mensagem no idioma em que deseja que ela apareça.

#### Configurando seu Collect Email {#configurando-collect-email}

Uma vez que você completou os pré-requisitos, você pode começar a configurar seu Collect Email.

As etapas para configurar isso são separadas em duas opções:

1. Use seu próprio Provedor de Serviços de E-mail. (PSE)

2. Use o PowerReviews como PSE.

##### Usando seu próprio PSE

Se você estiver usando seu próprio provedor de serviços de e-mail para enviar e-mails pós-compra, poderá incluir links **Write-a-Review** no seu e-mail para que os clientes deixem um comentário. Os links Write-a-Review (Escreva uma Avaliação) no seu email devem incluir DUAS variáveis-chave:

* pr_source=email

* pr_merchant_user_email=\<user email> * ( SE VOCÊ ESTÁ ENCRIPTANDO EMAIL USE PR_EMUID)

Por exemplo, um link Escreva-Uma-Avaliação pode ser assim para um determinado produto:

**http://www.nike.com.br/writeareview?pr_page_id=abc123&pr_source=email&pr_merchant_user_email=joe@i9xp.com.br&pr_merchant_user_id=12345**

As análises coletadas dessa maneira com as variáveis incluídas recebem o selo do comprador verificado no visor de análises.

Se você estiver usando seu próprio provedor de serviços de email (ESP), deverá criptografar os endereços de email.

[clique para instruções sobre como encriptar endereços de e-mail](encripting-emails.md)

#### Usando PowerReviews como seu Provedor de E-mails {#usando-power-reviews-como-seu-ep}

Para configurar seu Coletor de E-mails (Collect Email):

1. Navegue para o portal do PowerReviews.
2. Clique em **Setup** no menu de navegação.
3. Clique em **Email Manager** na página de produto.
![screenshot](img/Email&#32;update&#32;1_1013x327.png)
4. Digite as informações de e-mail necessárias. Você pode voltar e editar essas informações a qualquer momento. Para começar a enviar e-mails aos clientes, os campos necessários devem ser preenchidos.
 4.1 **From name** - O nome que aparece no campo "From" do e-mail. Como uma melhor prática, o PowerReviews recomenda usar o nome da sua empresa. Dessa forma, seu cliente sabe exatamente quem está enviando o e-mail assim que vê-lo em sua caixa de entrada.
 4.2 **Reply-to-Address** - O endereço de e-mail para onde você deseja que todas as respostas ao Collect Email sejam enviadas.
 4.3 **Subject** - A linha de assunto do seu e-mail. Por exemplo, "Avalie sua compra recente", ou "Avalie sua compra de "Marca".
  4.3.1 Para adicionar o primeiro nome do seu cliente para personalização, inclua {FIRST_NAME} na linha de assunto. O sistema PowerReviews retirará o nome das informações do pedido e a exibirá como parte do assunto para o cliente apropriado.
  4.3.2 Exemplo: "Oi {FIRST_NAME}, por favor, avalie sua compra recente."
 4.4 **Header Logo** (opcional) - seu logotipo da empresa/marca que será exibido no e-mail. Esta imagem será redimensionada para 250 px de largura, 75 px de altura.
 4.5 **Body Copy** - Personalize seu mensagem de e-mail.
 4.6 Selecione o tipo **Call to Action** (Chamada para Ação):
  4.6.1 **Stars**: Uma _call to action_ mostrando classificações de estrelas em branco. Quando um cliente clica na classificação de estrela de um produto, ele preenche automaticamente quando é redirecionado para o formulário Write-a-Review.
  4.6.2 **Button**: Uma _call to action_ com um botão Write-A-Review.
  4.6.3 **Links**: Uma _call to action_ com um link para Write-A-Review.
5. Clique **Save Content**.
6. Para receber uma prévia do seu e-mail, fique à vontade para enviar um e-mail de teste. Tudo o que você precisa fazer é digitar seu **endereço de e-mail** e clicar em **Send Test Email** (Enviar e-mail de teste).

 > :warning: O **Reply-to-Address** não é o endereço de e-mail do qual os e-mails virão. Todos os e-mails são originários de um endereço de e-mail powerreviewsemail.com que contém o nome da sua empresa. Você não pode editar este endereço.

 Além disso, você deve criptografar todos os e-mails enviados usando o Collect Email para criptografar os endereços de e-mail, para proteger qualquer informação pessoal identificável dentro do e-mail. Mais informações, consulte [Revisar suas compras](review-your-purchases.md).

#### Agendando seus E-mails {#agendando-emails}

 Depois de personalizar seu e-mail e configurar seu feed de pedidos, você pode configurar um cronograma para determinar quantos dias após a compra deseja enviar seus e-mails para seus clientes e ativar Collect Email. Se você usar o Checkout Beacon para alimentar sua coleta de e-mails, o PowerReviews assumirá que a data do pedido que o Beacon coleta é o dia em que o checkout ocorre. Considere esta data quando você agendar seus e-mails.

 Navegue de volta para a guia Agendar (Schedule) no Portal. Agora que seus itens de ação estão completos, você pode agendar seus e-mails.

Para Agendar e-mails:

1. Digite o número de dias após a compra que deseja enviar o primeiro e-mail. Como uma boa prática, o PowerReviews recomenda o envio do primeiro e-mail de 14 a 21 dias após a compra do seu cliente.
2. (Opcional) Digite o número de dias que deseja enviar um segundo e-mail depois que o primeiro e-mail for enviado.
3. Verifique se seu status está alterado para Ativado (Enabled).

> :warning: Se você quiser especificar a hora do dia em que seus e-mails são enviados através da propriedade FUE_SEND_AT comerciante, entre em contato com o seu Diretor de Sucesso do Cliente para que eles configurem isso para você. Como padrão, os e-mails serão enviados às 10:22 am CST.

#### Formato de coleção de revisão

* Dependendo do número de produtos normalmente incluídos no tamanho da cesta do seu cliente, temos duas opções diferentes para os clientes revisarem o conteúdo: (1) Revise suas compras (Review Your Purchases) (2) Formulário de Coleta Padrão (Standart Collection Form). Na aba '**Settings**' do Gerenciador de e-mails (Email Manager), você tem a capacidade de escolher entre essas duas opções.
* Review Your Purchases (RYP) é um recurso onde os clientes podem revisar vários produtos que compraram em uma única página, promovendo uma coleta e cobertura adicionais de revisão. Mais documentação sobre este recurso pode ser encontrada [aqui](review-your-purchases.md). Recomendamos que os clientes usem isso se tiverem um tamanho médio de cesta maior que 1.

![screenshot](img/Review&#32;Collection&#32;Format.png)

#### Solução de problemas

**meu código feedless inclui um image_url válido e a imagem do produto renderiza sem problema no formulário Write-A-Review e Moderation, mas os E-mails de coleta estão mostrando uma miniatura "no image available".**

Verifique como os URLs são construídos para a imagem. Se você ver o "+" onde o nome do arquivo tem um espaço, ele será codificado incorretamente. Substitua o "+" por "%20", e a imagem aparecerá em seus e-mails.
