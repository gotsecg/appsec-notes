JWT é um padrão para transmitir informações entre sistemas de forma segura.

Ele funciona como um "crachá digital" após o login, você fica com o token em cada requisição validando sua identidade.
A confiabilidade vem dessa assinatura digital, que garante que ninguém adulterou o token no caminho.

Essa assinatura pode ser feita de duas formas, sendo elas :
-um segredo compartilhado (HMAC)
-com chaves pública/privada (RSA ou ECDSA).

No dia a dia, uso JWT pra duas coisas:
autenticação (identificar o usuário em cada requisição) e troca de informações entre serviços com garantia de integridade.
