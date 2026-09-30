# Formato da história

```
### [ID] Título curto e concreto

**Como** [persona real, não "usuário"]
**Quero** [ação]
**Para** [resultado percebido — o porquê, não o quê]

**Critérios de aceite**
- Given [contexto] / When [ação] / Then [resultado observável]
- Given [contexto de erro] / When [ação] / Then [comportamento esperado no erro]

**Fora de escopo desta história:**
- (o que NÃO entra — evita scope creep no refinamento)

**Dependências:** (o que precisa existir antes)
**Tamanho:** P / M / G (a squad refina)
```

## Exemplo completo

### [AUTH-1] Mensagem de erro específica no login

**Como** cliente que errou a senha
**Quero** saber exatamente o que deu errado
**Para** conseguir corrigir sem ligar para o call center

**Critérios de aceite**
- Given uma senha incorreta / When eu tento entrar / Then vejo "Senha incorreta" e um link para recuperar
- Given um código 2FA expirado / When eu confirmo / Then vejo "Código expirado" e um botão para reenviar
- Given falha de conexão / When eu tento entrar / Then vejo "Sem conexão. Tente novamente." e o app não perde o que digitei

**Fora de escopo:** redesign da tela de login; biometria; mudança no fluxo de 2FA.
**Dependências:** instrumentação de erro (AUTH-0) para sabermos os tipos reais de falha.
**Tamanho:** P

## Regra do "Para"
Se o "Para" repete o "Quero" com outras palavras, a história não tem valor claro. Reescreva.
❌ "Quero ver mensagem de erro **para** ver a mensagem de erro."
✅ "Quero ver mensagem de erro **para** corrigir sozinho e não precisar ligar."
