---
title: "Sou Jornalista / Pesquisador / Gestor — Contexto, dados e cobertura do projeto"
page-layout: full
---

::: {.page-hero}

::: {.breadcrumb-nav style="background:transparent;border:none;padding:0 0 0.75rem;font-size:0.8rem;color:rgba(255,255,255,0.6);"}
[Início](index.html) <span class="sep">/</span> Sou Jornalista / Pesquisador / Gestor
:::

# Sou Jornalista / Pesquisador / Gestor

::: {.lead}
Contexto político e técnico, dados de impacto, comparações internacionais e materiais de apoio para cobertura jornalística, pesquisa acadêmica e gestão pública.
:::

:::

::: {.audience-section}

::: {.audience-tabs}

- [Sou Cidadão](cidadao.html)
- [Sou Negócio](negocio.html)
- [Sou Desenvolvedor](desenvolvedor.html)
- [Sou Jornalista / Pesquisador / Gestor](jornalista.html){.active}

:::

:::

::: {.page-content}

## Por que isso é uma notícia

Este projeto representa uma mudança de lógica na forma como o Estado brasileiro lida com identidade digital, e tem pelo menos três ângulos relevantes para cobertura:

**Privacidade vs. vigilância.** As soluções hoje disponíveis no mercado para verificação etária podem exigir que o cidadão entregue CPF, foto de documento ou dados biométricos sem que isso seja realmente necessário. Este projeto inverte essa lógica: a verificação acontece sem que nenhuma informação pessoal seja transferida.

**Soberania tecnológica.** O Brasil desenvolve sua própria infraestrutura de identidade digital baseada em código aberto e padrões internacionais, em área que toca diretamente direitos fundamentais.

**Impacto econômico para pequenos negócios.** A Lei 15.211/25 impõe obrigações de verificação etária a plataformas digitais. As soluções comerciais disponíveis podem ter custo alto para micro e pequenas empresas. Este projeto oferece uma alternativa pública e gratuita.

---

## O que é o projeto

A **Verificação de Idade com Credenciais Verificáveis** é uma iniciativa do **Ministério da Gestão e da Inovação em Serviços Públicos (MGI)** que cria um mecanismo técnico pelo qual plataformas digitais podem confirmar que um usuário é maior de 18 anos **sem receber qualquer dado pessoal** do cidadão: nem nome, nem CPF, nem qualquer identificador.

A infraestrutura é pública, gratuita e baseada em código aberto. O emissor das credenciais é o **gov.br**, plataforma que já conta com 173 milhões de contas cadastradas e serve como identidade digital oficial do cidadão brasileiro.

## Por que esse projeto existe

O crescimento do acesso de crianças e adolescentes a conteúdos inapropriados na internet tornou-se um desafio regulatório em dezenas de países. No Brasil, a **Lei 15.211/25 (ECA Digital)** estabelece obrigações concretas para plataformas digitais, mas deixa em aberto *como* verificar a idade sem criar novos riscos de privacidade.

As credenciais verificáveis resolvem a verificação etária, com criptografia de ponta: especificamente com **Provas de Conhecimento Zero (Zero-Knowledge Proofs)**, que permitem confirmar um fato ("é maior de 18 anos") sem revelar nenhuma informação subjacente.

## Dados e estatísticas

::: {.info-card}
**Contexto de uso da internet por crianças e adolescentes no Brasil**

- 95% das crianças de 9 a 17 anos usam a internet regularmente — [CGI.br, TIC Kids Online Brasil 2023](https://cetic.br/pt/pesquisa/kids-online/)
- 78% acessam conteúdos sem qualquer restrição etária efetiva — [CGI.br, 2023](https://cetic.br/pt/pesquisa/kids-online/)
- Mais de 40 países já aprovaram ou discutem legislação de verificação de idade online

:::

::: {.info-card}
**Impacto econômico estimado**

- Soluções comerciais de verificação etária podem ter valor inviável para MPEs com alto volume de acessos
- O Brasil tem mais de 20 milhões de micro e pequenas empresas com presença digital, número que tende a aumentar [SEBRAE, 2025](https://agenciasebrae.com.br/dados/brasil-bate-recorde-historico-na-abertura-de-pequenos-negocios/)
- A infraestrutura pública elimina esse custo para plataformas que aderirem ao ecossistema

:::

## Comparação com soluções internacionais

| País / Região | Solução | Privacidade | Soberania | Status |
|---|---|---|---|---|
| Reino Unido | Verificação por documento (upload de ID) | ❌ Baixa | ❌ Empresas privadas | Em produção |
| França | Verificação por operadora móvel | ⚠️ Parcial | ⚠️ Parcial | Em produção |
| União Europeia | EUDI Wallet (carteira digital europeia) | ✅ Alta | ✅ Alta | Em implantação |
| **Brasil** | **Credencial Verificável via gov.br** | ✅ Alta | ✅ Alta | **MVP em testes** |

A proposta brasileira é tecnicamente comparável à iniciativa europeia — e, em alguns aspectos, mais direta na implementação por ancorar-se numa infraestrutura de identidade digital (gov.br) já existente e em escala nacional.

## Fases do projeto

O projeto segue um modelo de implantação gradual, priorizando estabilidade técnica e confiança pública sobre velocidade de expansão:

- **Fase 0** — Desenvolvimento da especificação técnica e publicação do código no GitHub
- **Fase 1** — MVP com público restrito e plataformas parceiras *(em andamento)*
- **Fase 2** — Expansão para pilotos estratégicos por setor
- **Fase 3** — Abertura do Registro de Confiança para emissores certificados além do gov.br
- **Fase 4** — Disponibilização ampla e integração com carteiras de mercado

## Equipe e parceiros

O projeto é desenvolvido pelo **Ministério da Gestão e da Inovação em Serviços Públicos (MGI)** com os seguintes atores no ecossistema:

| Parceiro | Papel |
|---|---|
| Secretaria de Governo Digital (SGD) | Coordenação estratégica e supervisão técnica |
| Dataprev | Desenvolvimento e operação da infraestrutura |
| Autoridade Nacional de Proteção de Dados (ANPD) | Consulta regulatória e validação de conformidade com a LGPD |
| Ministério da Justiça e Segurança Pública | Alinhamento com ECA Digital e políticas de proteção de crianças |
| MOSIP / Inji (parceiro técnico internacional) | Plataforma de código aberto utilizada como base tecnológica |

## Kit de imprensa

::: {.press-kit}
Os materiais abaixo estão em preparação e serão disponibilizados ao longo da Fase 1 do projeto:

- Ficha técnica do projeto (PDF)
- Infográficos explicativos para publicação
- Descrição oficial para citação em matérias
- Contato para entrevistas com especialistas técnicos e gestores do projeto

**Contato para imprensa:** `[em breve]`

Para solicitações urgentes ou cobertura do piloto, entre em contato pelo [formulário de imprensa →](contato.html#imprensa).
:::

## Perguntas frequentes

**O projeto é obrigatório para todas as plataformas?**
Não. A Verificação de Idade é uma infraestrutura pública de adesão voluntária. A obrigatoriedade de verificar a idade dos usuários é determinada pela Lei 15.211/25; este projeto oferece a solução técnica para que plataformas cumpram essa obrigação de forma que respeita a privacidade do cidadão.

**Qual é a diferença entre isso e simplesmente pedir o CPF?**
Quando uma plataforma pede o CPF, ela recebe e armazena um dado pessoal sensível,  criando responsabilidade legal, risco de vazamento e potencial de rastreamento. Com a Credencial Verificável, a plataforma recebe apenas uma confirmação criptográfica ("maior de 18: sim"), sem nenhum dado identificável. É tecnicamente impossível rastrear o cidadão a partir dessa resposta.

**O governo conseguirá saber quais sites o cidadão acessa?**
Não. O gov.br emite a credencial, mas não é notificado quando ela é apresentada a uma plataforma. A arquitetura do sistema foi projetada especificamente para impedir esse rastreamento, inclusive por parte do governo emissor.

**Quanto custa para o cidadão?**
Zero. A obtenção e o uso da credencial são inteiramente gratuitos para cidadãos brasileiros com conta no gov.br nos níveis Prata ou Ouro.

**O projeto foi validado pela ANPD?**
A ANPD participa do ecossistema do projeto como parceira em consulta regulatória. A validação formal de conformidade com a LGPD está prevista para as fases subsequentes ao MVP.

[Acessar documentação técnica →](docs/index.html){.btn-secondary}
[Falar com a equipe →](contato.html){.btn-primary-govbr}

:::
