---
title: ""
page-layout: full
---

::: {.page-hero}

::: {.breadcrumb-nav style="background:transparent;border:none;padding:0 0 0.75rem;font-size:0.8rem;color:rgba(255,255,255,0.6);"}
[Início](index.html) <span class="sep">/</span> [Como funciona](como-funciona.html) <span class="sep">/</span> Como comprovar sem revelar identidade
:::

# Como comprovar idade sem revelar identidade

::: {.lead}
A criptografia moderna torna possível provar que você tem 18 anos ou mais sem revelar quem você é. Entenda como isso funciona.
:::

:::

::: {.subnav}
- [O que é Credencial Verificável](credencial-verificavel.html)
- [Como comprovar sem revelar identidade](comprovar-idade.html){.active}
- [Jornada do Usuário](jornada-usuario.html)
- [Perguntas Frequentes](faq.html)
:::

::: {.page-content}

## O problema que precisamos resolver

Imagine que você quer provar que é maior de 18 anos para acessar um serviço online. As opções tradicionais são problemáticas:

- **Enviar o CPF**: a plataforma agora tem seu CPF. Para sempre.
- **Tirar foto do RG**: a plataforma tem uma cópia do seu documento. Vazamentos?
- **Fornecer data de nascimento**: dado suficiente para rastreamento cruzado.

Todas essas abordagens revelam **mais do que o necessário**. O que o serviço realmente precisa saber é apenas: "esta pessoa tem 18 anos ou mais?"

## A solução: Divulgação Seletiva com Prova Criptográfica

A Verificação de Idade usa um mecanismo chamado **SD-JWT (Selective Disclosure JWT)** combinado com **assinaturas BBS+** para resolver exatamente esse problema.

A ideia central é: em vez de revelar o dado (sua data de nascimento), você revela apenas **uma prova matemática** de que o dado satisfaz a condição ("data de nascimento implica idade ≥ 18").

## Como funciona passo a passo

**1. O gov.br emite sua credencial com seus dados reais:**

```
Dados reais (nunca compartilhados):
  - Nome: Maria Silva
  - CPF: 123.456.789-00
  - Data de nascimento: 15/03/1985
  - Foto: [...]

Atributo derivado (o único que será compartilhado):
  - maior_de_18_anos: TRUE
```

**2. A assinatura cobre todos os atributos, incluindo o derivado:**

O gov.br assina matematicamente o pacote inteiro. A chave é que a assinatura BBS+ permite que, no futuro, você prove que um *subconjunto* dos atributos estava no pacote original — sem revelar os outros.

**3. Quando você precisa verificar sua idade:**

Você instrui seu wallet a criar uma **Verifiable Presentation** que inclui apenas o atributo `maior_de_18_anos: true`, acompanhado de uma prova matemática de que esse atributo foi assinado pelo gov.br como parte de uma credencial válida.

```
O que o verificador recebe:
  - maior_de_18_anos: true ✓
  - Prova BBS+: [sequência matemática]

O que o verificador NÃO recebe:
  - Nome: ???
  - CPF: ???
  - Data de nascimento: ???
```

**4. O verificador confere a matemática:**

O verificador usa a chave pública do gov.br (publicada de forma aberta) para verificar que a prova matemática é válida. Se for, ele sabe com certeza que o atributo veio de uma credencial legítima — sem precisar saber quais outros dados estavam nela.

## Por que o verificador não pode descobrir sua identidade?

Porque ele **nunca recebe** nenhuma informação que permita identificar você. O sistema é projetado para que:

- Dois verificadores diferentes não consigam correlacionar que atenderam o mesmo usuário (anti-correlação por design)
- Mesmo que o verificador colabore com o emissor, eles não conseguem descobrir quem você é a partir da prova
- A prova matemática é diferente a cada apresentação — não pode ser usada para rastreamento

## A analogia do cofre

> Imagine um cofre com vários compartimentos. O gov.br coloca seus dados em compartimentos diferentes e tranca com um cadeado especial. Quando você precisa provar sua idade, você abre **apenas aquele compartimento**, sem que ninguém consiga ver os outros — e eles verificam que o cadeado é mesmo do gov.br.

## Limitações e transparência

Nenhum sistema é perfeito. É importante ser transparente:

- **Confiança no emissor**: o sistema depende de você confiar que o gov.br é honesto. Se o gov.br fosse malicioso, poderia emitir credenciais falsas.
- **Segurança do dispositivo**: se seu dispositivo for comprometido, sua credencial pode ser usada por outra pessoa.
- **Metadados de rede**: o verificador sabe que *alguém* fez uma verificação (sem saber quem), o que pode gerar metadados agregados.

[Próximo: Jornada do Usuário →](jornada-usuario.html){.btn-primary-govbr}

:::
