---
title: ""
page-layout: full
---

::: {.page-hero}

::: {.breadcrumb-nav style="background:transparent;border:none;padding:0 0 0.75rem;font-size:0.8rem;color:rgba(255,255,255,0.6);"}
[Início](index.html) <span class="sep">/</span> [Como funciona](como-funciona.html) <span class="sep">/</span> Credencial Verificável
:::

# O que é uma Credencial Verificável?

::: {.lead}
Uma credencial digital com prova criptográfica que garante autenticidade sem revelar informações além do necessário.
:::

:::

::: {.subnav}
- [O que é Credencial Verificável](credencial-verificavel.html){.active}
- [Como comprovar sem revelar identidade](comprovar-idade.html)
- [Jornada do Usuário](jornada-usuario.html)
- [Perguntas Frequentes](faq.html)
:::

::: {.page-content}

## A ideia fundamental

Uma **Credencial Verificável** (*Verifiable Credential*, ou VC) é a versão digital de um documento físico como a carteira de motorista ou o passaporte, mas com superpoderes criptográficos.

Assim como um documento físico, ela:

- Afirma fatos sobre você (ex.: "nascido em 1990", "tem mais de 18 anos")
- É emitida por uma autoridade confiável
- Pode ser apresentada a qualquer pessoa que precise verificá-la

Mas diferente de documentos físicos, ela:

- Não pode ser falsificada (prova criptográfica inquebrável)
- Permite revelação seletiva (mostre apenas o que precisa)
- Não requer contato com o emissor para ser verificada
- Fica guardada no **seu** dispositivo, não em servidores de terceiros

## A anatomia de uma Credencial Verificável

Uma VC é composta por três partes principais:

::: {.info-card}
### 📋 Metadados da credencial

Informações sobre a própria credencial: quem a emitiu, quando foi emitida, quando expira, qual o seu tipo.

```
Tipo: AgeVerificationCredential
Emissor: gov.br (DID verificável)
Emissão: 2024-01-15
Validade: 2025-01-15
```
:::

::: {.info-card}
### 👤 Atributos (Claims)

Os fatos afirmados sobre o titular. No caso da Verificação de Idade, apenas um atributo é necessário:

```
maior_de_18_anos: true
```

Nada mais é incluído. Sem nome. Sem CPF. Sem data de nascimento exata.
:::

::: {.info-card}
### 🔐 Prova Criptográfica

Uma assinatura digital do emissor (gov.br) que garante que os atributos são autênticos e não foram modificados. Qualquer tentativa de alterar a credencial invalida a assinatura.
:::

## A diferença entre Credenciais Verificáveis e tokens JWT comuns

Você pode estar familiarizado com tokens JWT (JSON Web Token), usados amplamente em autenticação web. As VCs vão além:

| Característica | JWT comum | Verifiable Credential |
|----------------|-----------|----------------------|
| Revelação seletiva | ❌ Revela tudo | ✅ Apenas o necessário |
| Descentralização | ❌ Depende de servidor | ✅ Verificável offline |
| Padrão aberto | ⚠️ Parcial | ✅ W3C oficial |
| Prova de conhecimento zero | ❌ Não | ✅ Com BBS+ |
| Portabilidade | ⚠️ Limitada | ✅ Interoperável |

## O padrão W3C

As Credenciais Verificáveis são especificadas pelo **World Wide Web Consortium (W3C)** no documento [Verifiable Credentials Data Model 2.0](https://www.w3.org/TR/vc-data-model-2.0/). Isso garante que:

- Qualquer implementação compatível pode verificar credenciais de qualquer emissor
- O padrão é aberto, revisado publicamente e livre de royalties
- A implementação brasileira é interoperável com a da União Europeia, Reino Unido e outros países

## Onde a credencial fica guardada?

A credencial fica em um **wallet** (carteira digital), que é um aplicativo no seu dispositivo. O gov.br integra essa funcionalidade diretamente ao seu aplicativo.

> A credencial nunca sai do seu dispositivo sem sua autorização explícita. Não existe servidor centralizado guardando suas credenciais.

[Próximo: Como comprovar idade sem revelar identidade →](comprovar-idade.html){.btn-primary-govbr}

:::
