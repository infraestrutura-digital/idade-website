---
title: ""
page-layout: full
---

::: {.page-hero}

::: {.breadcrumb-nav style="background:transparent;border:none;padding:0 0 0.75rem;font-size:0.8rem;color:rgba(255,255,255,0.6);"}
[Início](index.html) <span class="sep">/</span> [Como funciona](como-funciona.html) <span class="sep">/</span> Perguntas Frequentes
:::

# Perguntas Frequentes

::: {.lead}
Tire suas dúvidas sobre privacidade, segurança e funcionamento da Verificação de Idade.
:::

:::

::: {.subnav}
- [O que é Credencial Verificável](credencial-verificavel.html)
- [Como comprovar sem revelar identidade](comprovar-idade.html)
- [Jornada do Usuário](jornada-usuario.html)
- [Perguntas Frequentes](faq.html){.active}
:::

::: {.page-content}

## Privacidade e Dados

<details class="faq-item">
<summary>O governo saberá quais sites acesso com a credencial?</summary>
<div class="faq-body">
Não. O fluxo de apresentação da credencial não envolve o emissor (gov.br). Quando você apresenta sua credencial a um serviço, a verificação é feita matematicamente — o serviço checa a assinatura criptográfica contra a chave pública publicada do gov.br, mas sem enviar nenhuma mensagem ao gov.br. O emissor não é notificado. Isso é uma propriedade fundamental do design do sistema.
</div>
</details>

<details class="faq-item">
<summary>O serviço que verificou minha credencial pode descobrir minha identidade?</summary>
<div class="faq-body">
Não. O serviço recebe apenas uma prova matemática de que você tem 18 anos ou mais, sem nenhum identificador pessoal. Além disso, cada apresentação gera uma prova diferente, então mesmo que dois serviços comparassem suas provas, eles não conseguiriam confirmar que se trata da mesma pessoa.
</div>
</details>

<details class="faq-item">
<summary>Minha credencial pode ser usada para me rastrear?</summary>
<div class="faq-body">
Não. A tecnologia de Apresentações Verificáveis com BBS+ garante anti-correlação por design. Cada vez que você apresenta a credencial, uma prova diferente é gerada. Não é possível para dois verificadores distintos — nem mesmo para o emissor — correlacionar que o mesmo usuário realizou duas verificações diferentes.
</div>
</details>

<details class="faq-item">
<summary>O que acontece com meus dados se meu celular for roubado?</summary>
<div class="faq-body">
Sua credencial está protegida pelo PIN, senha ou biometria do seu dispositivo. Para usá-la, é necessária autenticação biométrica ou PIN. Se seu celular for roubado, você pode revogar a credencial remotamente acessando o portal gov.br pelo computador. Após a revogação, qualquer tentativa de usar a credencial será rejeitada.
</div>
</details>

---

## Segurança

<details class="faq-item">
<summary>É possível falsificar uma credencial?</summary>
<div class="faq-body">
Na prática, não. A credencial é protegida por criptografia assimétrica com curvas elípticas — o mesmo tipo de criptografia que protege transações bancárias. Para falsificar a assinatura do gov.br, seria necessário quebrar esse algoritmo, o que está além das capacidades computacionais atuais e previstas para os próximos anos.
</div>
</details>

<details class="faq-item">
<summary>E se o sistema do gov.br for hackeado?</summary>
<div class="faq-body">
O design do sistema minimiza os impactos de um eventual comprometimento. Como as credenciais ficam nos dispositivos dos usuários (não em servidores centrais), um hack no gov.br não expõe credenciais emitidas. O pior cenário seria a emissão de credenciais fraudulentas — algo que pode ser mitigado com rotação de chaves e revogação de certificados comprometidos.
</div>
</details>

<details class="faq-item">
<summary>Com que frequência preciso renovar a credencial?</summary>
<div class="faq-body">
A credencial tem validade de 12 meses. O app gov.br avisa quando ela está próxima de expirar. A renovação é automática, gratuita e leva menos de um minuto diretamente no aplicativo, sem necessidade de nenhuma verificação adicional.
</div>
</details>

---

## Acesso e Uso

<details class="faq-item">
<summary>A verificação é obrigatória? Tenho que usá-la?</summary>
<div class="faq-body">
A infraestrutura de Verificação de Idade é voluntária para os cidadãos. Cabe a cada plataforma decidir quais métodos de verificação aceitar. Em geral, as plataformas devem oferecer alternativas para cidadãos que não queiram ou não possam usar o sistema — embora algumas soluções alternativas possam ser menos privadas.
</div>
</details>

<details class="faq-item">
<summary>E se eu não tiver smartphone?</summary>
<div class="faq-body">
O sistema atual é baseado em smartphone. O governo está explorando soluções para cidadãos sem acesso a dispositivos móveis, incluindo verificação presencial em agências do governo e parceiros credenciados. Fique atento às atualizações do gov.br para essas modalidades.
</div>
</details>

<details class="faq-item">
<summary>Quanto custa para o cidadão?</summary>
<div class="faq-body">
A obtenção e o uso da credencial são completamente gratuitos para cidadãos. É uma infraestrutura pública financiada pelo governo federal, sem nenhum custo para o usuário.
</div>
</details>

<details class="faq-item">
<summary>Posso usar a mesma credencial em vários serviços?</summary>
<div class="faq-body">
Sim. A credencial emitida pode ser apresentada em qualquer serviço que aceite a Verificação de Idade, sem limite de usos e sem custo adicional. Cada apresentação é independente e não cria vínculo entre os serviços que você acessou.
</div>
</details>

---

## Técnico

<details class="faq-item">
<summary>Precisa de internet para usar a credencial?</summary>
<div class="faq-body">
Para emissão e renovação, sim. Para apresentação da credencial em serviços compatíveis, em geral não — a verificação pode ser feita offline pelo verificador, pois é baseada em criptografia local. Mas alguns verificadores podem exigir conexão para checagem em tempo real de revogação.
</div>
</details>

<details class="faq-item">
<summary>O sistema é compatível com outros países?</summary>
<div class="faq-body">
Sim. Por ser baseado nos padrões W3C (Verifiable Credentials e DIDs) e OpenID4VP, o sistema brasileiro é interoperável com implementações de outros países, incluindo o EUDI Wallet da União Europeia. Acordos de reconhecimento mútuo ainda dependem de negociação diplomática.
</div>
</details>

<details class="faq-item">
<summary>Onde posso ver o código-fonte do sistema?</summary>
<div class="faq-body">
Os componentes de infraestrutura são de código aberto e estão disponíveis no repositório oficial do CIPD no GitHub. Qualquer pessoa pode auditar, reportar vulnerabilidades ou contribuir com melhorias seguindo as diretrizes de contribuição do projeto.
</div>
</details>

[Não encontrou sua resposta? Entre em contato →](mailto:contato@infraestrutura.digital){.btn-primary-govbr}

:::
