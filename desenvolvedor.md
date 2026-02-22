---
title: ""
page-layout: full
---

::: {.page-hero}

::: {.breadcrumb-nav style="background:transparent;border:none;padding:0 0 0.75rem;font-size:0.8rem;color:rgba(255,255,255,0.6);"}
[Início](index.html) <span class="sep">/</span> Sou Desenvolvedor
:::

# Sou Desenvolvedor

::: {.lead}
Documentação técnica completa, SDKs e ambiente de testes para integrar a Verificação de Idade na sua aplicação.
:::

:::

::: {.audience-section}

::: {.audience-tabs}

- [Sou Cidadão](cidadao.html)
- [Sou Negócio](negocio.html)
- [Sou Desenvolvedor](desenvolvedor.html){.active}
- [Sou Jornalista / Gestor](jornalista.html)

:::

:::

::: {.page-content}

## Visão Geral da Arquitetura

A Verificação de Idade é baseada no protocolo **W3C Verifiable Credentials** combinado com **Decentralized Identifiers (DIDs)**. O fluxo segue o padrão **OpenID4VP (OpenID for Verifiable Presentations)**.

```
Usuário (Holder)          Verifier (sua app)         Issuer (gov.br)
     │                          │                          │
     │  1. Solicitar acesso      │                          │
     │ ─────────────────────►   │                          │
     │                          │                          │
     │  2. Presentation Request  │                          │
     │ ◄─────────────────────   │                          │
     │                          │                          │
     │  3. Apresentar VC         │                          │
     │ ─────────────────────►   │                          │
     │                          │  4. Verificar assinatura  │
     │                          │ ─────────────────────►   │
     │                          │                          │
     │                          │  5. Confirmação           │
     │                          │ ◄─────────────────────   │
     │  6. Acesso concedido      │                          │
     │ ◄─────────────────────   │                          │
```

## Padrões e Especificações

A infraestrutura é construída sobre os seguintes padrões abertos:

- **W3C Verifiable Credentials Data Model 2.0** — estrutura dos atributos verificáveis
- **W3C Decentralized Identifiers (DIDs) v1.0** — identificação descentralizada
- **OpenID for Verifiable Presentations (OID4VP)** — protocolo de apresentação
- **SD-JWT (Selective Disclosure JWT)** — divulgação seletiva de atributos
- **BBS+ Signatures** — assinaturas de divulgação seletiva com prova de conhecimento zero

## Estrutura da Credencial

```json
{
  "@context": [
    "https://www.w3.org/2018/credentials/v1",
    "https://idade.infraestrutura.digital/context/v1"
  ],
  "type": ["VerifiableCredential", "AgeVerificationCredential"],
  "issuer": "did:web:infraestrutura.digital",
  "issuanceDate": "2024-01-15T00:00:00Z",
  "expirationDate": "2025-01-15T00:00:00Z",
  "credentialSubject": {
    "id": "did:key:z6Mk...",
    "ageOver18": true
  },
  "proof": {
    "type": "BbsBlsSignature2020",
    "created": "2024-01-15T00:00:00Z",
    "verificationMethod": "did:web:infraestrutura.digital#key-1",
    "proofPurpose": "assertionMethod",
    "proofValue": "..."
  }
}
```

## Endpoint de Verificação

### `POST /api/v1/verify`

Valida uma Verifiable Presentation recebida do usuário.

**Request:**

```json
{
  "vp_token": "eyJhbGciOiJFUzI1NiIsInR5cCI6IkpXVCJ9...",
  "presentation_submission": {
    "id": "...",
    "definition_id": "age-verification-request",
    "descriptor_map": [...]
  }
}
```

**Response 200 OK:**

```json
{
  "verified": true,
  "age_over_18": true,
  "issued_by": "gov.br",
  "credential_expires": "2025-01-15T00:00:00Z"
}
```

**Response 400 — Credencial inválida:**

```json
{
  "verified": false,
  "error": "INVALID_PROOF",
  "message": "A assinatura da credencial é inválida ou expirou."
}
```

## SDKs Disponíveis

| Linguagem | Repositório | Status |
|-----------|-------------|--------|
| **JavaScript / TypeScript** | `@cipd/age-verification-js` | ✅ Estável |
| **Python** | `cipd-age-verification` | ✅ Estável |
| **Java / Kotlin** | `br.gov.cipd:age-verification` | 🔄 Beta |
| **Go** | `github.com/cipd/age-verification-go` | 🔄 Beta |

## Ambiente Sandbox

Use o ambiente de testes para integrar sem impacto em produção:

- **Base URL:** `https://sandbox.idade.infraestrutura.digital`
- **DID do Emissor (Sandbox):** `did:web:sandbox.infraestrutura.digital`
- **Credenciais de teste:** geradas automaticamente pelo CLI de testes

```bash
# Instalar CLI de testes
npm install -g @cipd/age-verification-cli

# Gerar credencial de teste
cipd-age-verify generate-test-credential --did did:key:z6Mk...

# Simular fluxo completo
cipd-age-verify simulate-flow --verifier-url https://meuapp.com.br
```

## Requisitos de Segurança

::: {.callout-important}
### Não armazene o vp_token

O token de apresentação é de uso único e não deve ser armazenado. Seu sistema deve armazenar apenas o resultado da verificação (`verified: true/false`) com carimbo de tempo.
:::

::: {.callout-note}
### Rotação de chaves

O emissor rotaciona suas chaves de assinatura periodicamente. Seu sistema deve buscar o documento DID atualizado a cada verificação, nunca cachear a chave por mais de 24 horas.
:::

## Suporte técnico

Para dúvidas técnicas, abra uma issue no repositório oficial ou envie e-mail para `dev@infraestrutura.digital`.

[Acessar repositório no GitHub →](https://github.com/cipd){.btn-primary-govbr}

:::
