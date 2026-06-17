Vulnerabilidades Comuns

1. Algorithm Confusion (CVE crítica)
O atacante muda o 'alg' no header de 'RS256' para 'HS256' e assina com a chave pública.

json
Header manipulado pelo atacante
{ "alg": "HS256", "typ": "JWT" }
Assina com a chave PÚBLICA do servidor como se fosse o segredo HMAC
Mitigação: Sempre especifique explicitamente o algoritmo esperado na verificação.

---

2. Algorithm None
Alguns servidores aceitam tokens sem assinatura quando 'alg': "none"`.

json
{ "alg": "none", "typ": "JWT" }
Mitigação: Rejeite qualquer token com `alg: "none"`.

---

### 3. Weak Secret (Brute Force)
Segredos fracos como "secret" ou "123456" podem ser descobertos por força bruta.
Mitigação: Use segredos aleatórios com no mínimo 32 caracteres.

---

4. JWT Stored in localStorage (XSS)
Scripts maliciosos podem roubar o token do localStorage.
Mitigação: Armazene Access Tokens em memória e Refresh Tokens em cookies HttpOnly.

---

5. Missing Claims Validation
Verificar apenas a assinatura sem checar 'exp', 'iss' e 'aud'.
Mitigação: Sempre valide todas as claims relevantes.

