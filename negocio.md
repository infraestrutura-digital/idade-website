---
title: "Sou Negócio — Verificação etária sem coletar dados dos seus usuários"
page-layout: full
---

::: {.page-hero}

::: {.breadcrumb-nav style="background:transparent;border:none;padding:0 0 0.75rem;font-size:0.8rem;color:rgba(255,255,255,0.6);"}
[Início](index.html) <span class="sep">/</span> Sou Negócio
:::

# Sou Negócio

::: {.lead}
Uma infraestrutura pública e gratuita para verificar a idade dos seus usuários sem que sua plataforma precise coletar dados pessoais.
:::

:::

::: {.audience-section}

::: {.audience-tabs}

- [Sou Cidadão](cidadao.html)
- [Sou Negócio](negocio.html){.active}
- [Sou Desenvolvedor](desenvolvedor.html)
- [Sou Jornalista / Pesquisador / Gestor](jornalista.html)

:::

:::

::: {.page-content}

## Uma nova opção para o mercado

A **Lei 15.211/25 (ECA Digital)** criou obrigações reais de verificação etária para plataformas digitais brasileiras. Cumprir essa exigência, até agora, exigia contratar soluções de mercado com custo por verificação, o que funciona bem para grandes plataformas, mas pode representar uma barreira significativa para micro e pequenas empresas.

A Verificação de Idade com Credenciais Verificáveis é uma infraestrutura pública que torna esse compliance acessível para qualquer tamanho de negócio, **de forma gratuita**, sem que sua plataforma precise armazenar ou processar dados pessoais dos usuários.

## O que muda para o seu negócio

:::: {.columns}

::: {.column width="50%"}
::: {.info-card}
### Custo zero de infraestrutura
A plataforma é pública e gratuita para negócios de qualquer porte. Você paga apenas pelo desenvolvimento da integração uma vez.
:::
:::

::: {.column width="50%"}
::: {.info-card}
### Sem responsabilidade sobre dados sensíveis
Sua plataforma não recebe nem armazena CPF, foto de documento ou qualquer dado pessoal. Isso reduz drasticamente sua exposição à LGPD.
:::
:::

::::

:::: {.columns}

::: {.column width="50%"}
::: {.info-card}
### Conformidade com a Lei 15.211/25
Atenda aos requisitos do ECA Digital com um mecanismo reconhecido, baseado em padrão técnico aberto e auditável.
:::
:::

::: {.column width="50%"}
::: {.info-card}
### Infraestrutura nacional
Baseado na identidade digital do gov.br, com 173 milhões de contas cadastradas. Sem dependência de fornecedores estrangeiros.
:::
:::

::::

## Como funciona na prática

Do ponto de vista do seu negócio, o fluxo é simples:

1. Seu usuário tenta acessar um conteúdo ou serviço com restrição de idade
2. Sua plataforma solicita a verificação
3. O usuário confirma no próprio celular, usando a credencial que já obteve pelo gov.br
4. Sua plataforma recebe apenas **"maior de 18: sim"** — nada mais

Nenhum CPF, nenhuma foto, nenhum dado pessoal passa pela sua plataforma. A verificação é feita entre o usuário e o governo; você recebe apenas o resultado.

A integração técnica é feita pela sua equipe de desenvolvimento. [Veja a documentação técnica →](desenvolvedor.html)

## Casos de uso por setor

::: {.use-case}
**E-commerce (bebidas, tabaco, produtos controlados)**
Cumpra a exigência de verificação etária sem criar fluxos de coleta de documentos, reduzindo fricção na navegação de prudutos em exposição. 
:::

::: {.use-case}
**Games e plataformas digitais**
Atenda às exigências do ECA Digital para jogos com classificação etária sem onboarding complexo para usuários adultos.
:::

::: {.use-case}
**Aplicativos de relacionamento**
Implemente verificação etária obrigatória cumprindo a lei sem construir uma base de documentos dos seus usuários.
:::

::: {.use-case}
**Serviços financeiros com restrição etária**
Adicione uma camada de verificação etária complementar ao seu processo de onboarding regulatório existente.
:::

## Como sua plataforma pode integrar

A infraestrutura funciona em três cenários principais:

| Cenário | Como funciona |
|---|---|
| **Site ou web app** | Usuário é redirecionado brevemente ao wallet e retorna com a confirmação |
| **App mobile** | Abertura direta do app gov.br no celular do usuário |
| **Ambiente físico ou híbrido** | Usuário escaneia um QR code e confirma no celular |

## Perguntas frequentes

**E se o meu usuário não tiver conta no gov.br?**
A credencial exige conta gov.br nos níveis Prata ou Ouro. Usuários sem esse cadastro precisarão criá-lo. O processo é gratuito e leva alguns minutos. 

**Preciso assinar algum contrato ou termo de adesão?**
O modelo de adesão está sendo definido durante a fase de testes. Plataformas interessadas em participar do piloto devem entrar em contato com a equipe.

**Qual é a disponibilidade da infraestrutura?**
O SLA formal será publicado antes da abertura pública. Durante a fase de testes, a infraestrutura opera com monitoramento contínuo pela equipe técnica da Dataprev.

**A solução pode ser usada junto com outras formas de verificação que já uso?**
Sim. A Verificação de Idade com Credenciais Verificáveis pode ser adicionada como uma opção dentro de um fluxo que já inclui outras soluções, sem substituição obrigatória.

**Como funciona durante o período de testes?**
O acesso ao ambiente de sandbox está disponível para desenvolvedores desde já. Plataformas que queiram integrar em produção durante o piloto devem manifestar interesse pelo formulário abaixo.

::: {.cta-block}
[Quero participar do piloto →](contato.html#piloto){.btn-primary-govbr}
[Ver documentação técnica →](desenvolvedor.html){.btn-secondary}

:::

:::
