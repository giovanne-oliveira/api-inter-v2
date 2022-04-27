# CANCELAR BOLETO-INTER

## Cancelar Boleto
Cancelar o boleto<br>
Necessita informar o nossoNumero.

```php
    $dd = new stdClass;
    $dd->certificate = '../cert/Inter_API_Certificado.crt';//local do certifiado crt
    $dd->certificateKey = '../cert/Inter_API_Chave.key';//local do certifiado key
    $dd->client_id = '';//seu client_id
    $dd->client_secret = '';//client_secret
    $dd->token_auto = 1;//1=não; 2=sim (caso tiver 1 é obrigado a informar o token, caso contrário a API irá gerar o token automaticamente)
    $dd->token = '';//informe o token
    $dd->nossoNumero = '';//caso não informar traz o saldo do dia

    
    $bankingInter = new InterBanking($dd);

    $cancelarBoleto = $bankingInter->cancelarBoleto();
    print_r($cancelarBoleto);
```