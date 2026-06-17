✅ Fazer:

- Use HTTPS sempre — JWTs transmitidos via HTTP podem ser interceptados
- Defina expiração ('exp') — Nunca crie tokens sem prazo de validade
- Use segredos longos e aleatórios' — Mínimo 256 bits para HS256
- Valide todas as claims — 'iss', 'aud', 'exp' devem ser verificados
- Armazene Access Token em memória — Evita ataques XSS
- Use cookie HttpOnly para Refresh Token — Protege contra XSS
- Implemente rotação de Refresh Tokens — Detecta roubo de tokens
- Use algoritmos assimétricos em produção — RS256 ou ES256

❌ Não fazer:

- Não armazene JWTs no localStorage — Vulnerável a XSS
- Não coloque dados sensíveis no payload — É apenas Base64, não criptografia
- Não use o algoritmo 'none' — Permite tokens sem assinatura
- Não confie no 'alg' do header sem validação — Vulnerável a ataques
- Não crie tokens sem expiração — Tokens comprometidos ficam válidos para sempre
