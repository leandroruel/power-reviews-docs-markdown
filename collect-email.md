![logo](img/PR_logo.png)

# Coletar Email

Configurar um e-mail de pós-compra é essencial para obter mais avaliações adicionados aos produtos em seu site.

Usando **Collect Email** (Coletar Email), você pode enviar e-mails de acompanhamento aos seus clientes após a compra de um produto, convidando-os a escrever uma avaliação. Estudos mostram que até 60-80% das avaliações de clientes são resultado de solicitações por email.

Esta página contém as seguintes seções:
* [Pré-requisitos](#pre-requisitos)

* [Configurando Collect Email](#configurando-collect-email)

  * [Usando PowerReviews como seu Provedor de E-mails]()

* [Agendando seus e-mails]()

#### Pré-requisitos {#pre-requisitos}

Para implementar com êxito o Collect Email, verifique se você atendeu aos seguintes pré-requisitos:

* Ative o programa de e-mail PowerReviews. Para obter mais informações sobre como fazer isso, entre em contato com a equipe de implementação ou o diretor de sucesso do cliente, se você estiver fora de implementação.
* A coleta de email é direcionada pelos dados do pedido. Leia mais sobre como o PowerReviews pode ingerir os dados do seu pedido para decidir a melhor opção para o seu programa. Consulte [Opções e considerações dos dados do pedido]() para obter detalhes.
* Verifique se a página Write-A-Review (Escreva uma Avaliação) está definida e configurada corretamente. Você deve fornecer o URL Write-A-Review para o PowerReviews quando optar por usar o Collect Email.

**Se essa URL mudar, você deverá notificar o PowerReviews para atualizar as configurações da sua conta.**

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
