---
title: ""
page-layout: full
---

::: {.page-hero}

::: {.breadcrumb-nav style="background:transparent;border:none;padding:0 0 0.75rem;font-size:0.8rem;color:rgba(255,255,255,0.6);"}
[Início](index.html) <span class="sep">/</span> Sou Negócio
:::

# Sou Negócio

::: {.lead}
Integre a Verificação de Idade na sua plataforma de forma simples, segura e em conformidade com a legislação brasileira.
:::

:::

::: {.audience-section}

::: {.audience-tabs}

- [Sou Cidadão](cidadao.html)
- [Sou Negócio](negocio.html){.active}
- [Sou Desenvolvedor](desenvolvedor.html)
- [Sou Jornalista / Gestor](jornalista.html)

:::

:::

::: {.page-content}

## Por que integrar a Verificação de Idade?

Plataformas que disponibilizam conteúdo ou serviços voltados a adultos têm a **responsabilidade legal** de garantir que menores de 18 anos não tenham acesso. A Verificação de Idade oferece a forma mais segura, privada e juridicamente robusta de cumprir essa obrigação.

## Vantagens para o seu negócio

:::: {.columns}

::: {.column width="50%"}

::: {.info-card}
### ✅ Conformidade Legal
Atenda aos requisitos do **ECA**, do **Marco Civil da Internet** e das normas de proteção de menores sem necessidade de coletar dados adicionais dos seus usuários.
:::

:::

::: {.column width="50%"}

::: {.info-card}
### 🔒 Sem Responsabilidade sobre Dados
Como a verificação é feita pelo usuário diretamente, sua plataforma **não recebe nem armazena** dados sensíveis. Isso reduz drasticamente sua exposição à LGPD.
:::

:::

::::

:::: {.columns}

::: {.column width="50%"}

::: {.info-card}
### ⚡ Integração Simples
A API é aberta, documentada e segue padrões W3C. Equipes de desenvolvimento conseguem integrar em poucas horas com SDKs disponíveis nas principais linguagens.
:::

:::

::: {.column width="50%"}

::: {.info-card}
### 🇧🇷 Infraestrutura Nacional
Baseado na identidade digital do governo federal, com alta disponibilidade e suporte técnico. Sem dependência de fornecedores privados estrangeiros.
:::

:::

::::

## Como funciona a integração

O fluxo técnico é simples e não exige modificações profundas na sua arquitetura:

1. **Usuário inicia** o processo de acesso ao conteúdo restrito na sua plataforma
2. **Sua plataforma** gera um desafio de verificação e redireciona para o wallet do usuário
3. **Usuário apresenta** sua Credencial de Verificação de Idade ao seu sistema
4. **Sua plataforma recebe** apenas o resultado: `{ "maior_de_18": true }` com assinatura criptográfica verificável
5. **Acesso concedido** — sem nenhum dado pessoal trafegado

## Casos de uso comuns

- Plataformas de streaming com conteúdo para adultos
- E-commerces que vendem produtos com restrição de idade (bebidas, tabaco, etc.)
- Plataformas de jogos e apostas online
- Aplicativos de relacionamento
- Serviços financeiros com restrição etária

## Modelos de integração disponíveis

| Tipo | Descrição | Indicado para |
|------|-----------|---------------|
| **Redirect Flow** | Usuário é redirecionado ao wallet e retorna com prova | Web apps |
| **Deep Link** | Abertura direta do app gov.br no mobile | Apps móveis |
| **QR Code** | Usuário escaneia QR e confirma no celular | Ambientes físicos/híbridos |

## Próximos passos

Acesse a documentação técnica completa para desenvolvedores e o ambiente de testes (sandbox).

[Ver documentação técnica →](desenvolvedor.html){.btn-primary-govbr}

:::
