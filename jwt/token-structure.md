Estrutura do Token

Um token JWT é composto por três partes separadas por pontos ( . )


xxxxx.yyyyy.zzzzz
  │      │      │
Header Payload Signature


Exemplo:

eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJzdWIiOiIxMjM0NTY3ODkwIiwibmFtZSI6IkpvaG4gRG9lIiwiaWF0IjoxNTE2MjM5MDIyfQ.SflKxwRJSMeKKF2QT4fwpMeJf36POk6yJV_adQssw5c

1. Header

Contém o tipo do token e o algoritmo de assinatura.
json
{
  "alg": "HS256",
  "typ": "JWT"
}
Codificado em **Base64URL**.
---

2. Payload (Claims)

Contém as "afirmações" (claims) — informações sobre o usuário e metadados.
json
{
  "sub": "1234567890",
  "name": "João Silva",
  "email": "joao@email.com",
  "role": "admin",
  "iat": 1716239022,
  "exp": 1716242622
}


Claims Registered mais importantes:

| Claim | Nome | Descrição |
|-------|------|-----------|
| 'iss' | Issuer | Quem emitiu o token |
| 'sub' | Subject | ID do usuário/entidade |
| 'aud' | Audience | Para quem o token se destina |
| 'exp' | Expiration | Timestamp de expiração |
| 'iat' | Issued At | Timestamp de criação |
| 'jti' | JWT ID | Identificador único do token |

