# Criptografando Endereços de E-mail

O PowerReviews exige criptografar os endereços de e-mail do cliente se você usar o seu próprio [PSE](encripting-emails.md "Provedor de Serviços de Email") para garantir a privacidade do cliente ao enviar comentários.

Ao forçar a criptografia de endereço de email, o URL do formulário Write-A-Review não aceita endereços de email em texto não criptografado, mesmo que o endereço de email do cliente exista no banco de dados do PowerReviews. Também é importante observar que você não pode passar o parâmetro **pr_merchant_user_email** para gerar seu formulário Escreva uma Avaliação. Em vez disso, esse parâmetro é substituído por **pr_emuid** e o valor associado a esse parâmetro é uma versão criptografada do endereço de e-mail do seu cliente.

Se você não estiver usando o Collect Email para enviar emails de pós-compra, deverá usar o parâmetro **pr_emuid**, em vez de usar o parâmetro **pr_merchant_user_email** no URL.

PowerReviews usa um Cypher 128-bit AES/CTR/NoPadding, junto com o algoritmo AES.

Para criptografar strings de endereço de e-mail quando estiver usando seu próprio PSE, entre em contato com seu Engenheiro de Implementação se você ainda estiver implementando ou com o suporte do PowerReviews se você já é um cliente.

Depois que o engenheiro de implementação ou o suporte do PowerReviews fornecer as informações necessárias para criptografar a string, use as seguintes etapas para concluir o processo:

1. A string de e-mail deve estar em Lowercase.

2. Criptografar o e-mail usando AES Cypher, com a string de 16 dígitos única fornecida pelo PowerReviews como chave de criptografia (encryption key) e  'EmailPWRIVSpecIV' como o IV.

3. Converter qualquer caractere '+' para '==PLUS=='na string de email criptografada no passo 2.

4. Use URL encode na string do passo 3 usando UTF-8 encoding.

5. Atribua a string resultante ao parâmetro **pr_emuid** na URL da página de invólucro Write-A-Review.

Se você não estiver usando o Collect Email para enviar e-mails de pós-compra, você deve usar o parâmetro **pr_emuid**, em vez de usar o parâmetro **pr_merchant_user_email** na URL.

**! Se você optar por criptografar endereços de e-mail em SEUS e-mails de coleta, você deve usar o parâmetro pr_emuid em vez do pr_merchant_user_email..**
