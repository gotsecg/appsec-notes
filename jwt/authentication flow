Fluxo de Autenticação

Cliente                          Servidor
   │                                │
   │──── POST /login ──────────────►│
   │     { email, password }        │
   │                                │ Valida credenciais
   │                                │ Gera JWT
   │◄─── { token: "eyJ..." } ────── │
   │                                │
   │──── GET /api/dados ───────────►│
   │     Authorization: Bearer eyJ  │ Verifica assinatura
   │                                │ Verifica expiração
   │◄─── { dados protegidos } ───── │
   │                                │


Estratégia com Access + Refresh Token:


┌─────────────────────────────────────────────────────┐
│  Access Token                                       │
│  • Vida curta (15min ~ 1h)                          │
│  • Enviado em cada requisição                       │
│  • Armazenado em memória (não em localStorage)      │
└─────────────────────────────────────────────────────┘

┌─────────────────────────────────────────────────────┐
│  Refresh Token                                      │
│  • Vida longa (7d ~ 30d)                            │
│  • Usado apenas para obter novo Access Token        │
│  • Armazenado em cookie HttpOnly                    │
└─────────────────────────────────────────────────────┘
