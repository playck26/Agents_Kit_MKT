# FRAMEWORK DE DIAGNÓSTICO — TECNOLOGIA & VAREJO
## Documento de conhecimento do Agente de Diagnóstico & Onboarding

Este documento contém os blocos de perguntas que o agente deve cobrir durante a entrevista de onboarding. Adapte a ordem e profundidade ao vertical e maturidade do cliente.

---

## BLOCO 1 — NEGÓCIO E OFERTA

**Objetivo:** entender o que a empresa vende, pra quem, e qual o modelo econômico.

### Perguntas comuns (Tech e Varejo)
- O que vocês vendem? (Produto/serviço específico, não só categoria)
- Quem compra? (Persona/ICP — cargo, perfil, dor)
- Qual o ticket médio?
- Qual o ciclo de venda? (Tempo do primeiro clique até a compra)
- Quem são os 2-3 principais concorrentes diretos?
- Qual a oferta principal que vocês querem promover hoje? (Produto, plano, promoção, lançamento)

### Perguntas específicas — Tecnologia
- Modelo de receita: assinatura mensal/anual, licença única, freemium, uso?
- Tem trial gratuito ou demo? Quanto dura?
- O produto é self-service ou tem time de vendas envolvido?
- Qual o churn mensal? (Se SaaS)
- Tem expansion revenue (upsell, cross-sell)?
- O comprador é o usuário final ou alguém compra pra outra pessoa usar? (Ex: TI compra pra time de marketing)

### Perguntas específicas — Varejo
- E-commerce próprio, marketplace (Mercado Livre, Amazon, Shopee), loja física, ou combinação?
- Qual a margem média sobre o ticket?
- Qual o mix de produtos? (Concentrado em poucos SKUs ou diluído?)
- Tem sazonalidade forte? (Datas que concentram receita)
- Qual a taxa de recompra? Em quanto tempo o cliente volta?
- Frete grátis acima de qual valor?

---

## BLOCO 2 — MÉTRICAS DE NEGÓCIO

**Objetivo:** ter os números que servem de baseline pros próximos agentes.

- CAC atual (médio dos últimos 3 meses)
- LTV (se conseguir calcular)
- Razão LTV:CAC
- Faturamento mensal médio
- % do faturamento vindo de tráfego pago
- Meta de crescimento pros próximos 3-6 meses

### Específico Tech
- MRR / ARR
- Conversão de trial → pago
- Tempo médio até primeira receita

### Específico Varejo
- Ticket médio
- Itens por pedido
- Taxa de conversão do site
- Taxa de abandono de carrinho

---

## BLOCO 3 — OPERAÇÃO DE TRÁFEGO ATUAL

**Objetivo:** entender a maturidade e o histórico da conta.

- Há quanto tempo investem em tráfego pago?
- Quanto investem por mês hoje, separado por plataforma (Meta vs Google)?
- Quem opera hoje? (In-house, freelancer, agência)
- ROAS atual médio (e por plataforma se possível)
- Tem pixel/tag implementado e validado? Conversões offline integradas? (Importante pra Meta)
- Tem GA4 e Google Tag Manager configurados? Eventos de conversão funcionando?
- Tem CAPI (Conversions API) implementada na Meta?
- Estrutura atual de campanhas: quantas campanhas ativas? Por objetivo?
- Quais públicos estão usando hoje? (Lookalikes, interesses, retargeting, ABO/CBO)

---

## BLOCO 4 — CRIATIVO E COMUNICAÇÃO

**Objetivo:** entender o estado dos criativos e da mensagem.

- Quem produz criativo hoje? (Designer in-house, freelancer, agência, IA)
- Quantos criativos novos por semana/mês?
- Qual o formato dominante? (Estático, vídeo curto, carrossel, UGC)
- Tem banco de criativos antigo? Já testou várias variações?
- Quais são os 2-3 criativos com melhor performance histórica? (Pedir prints/links se possível)
- Tem identidade visual consolidada? Manual de marca?
- Tom de voz definido?

---

## BLOCO 5 — FUNIL E LANDING

**Objetivo:** entender o que acontece DEPOIS do clique.

- Pra onde o tráfego é mandado? (Landing específica, home, página de produto, WhatsApp, formulário)
- A landing foi feita pensando no anúncio ou é genérica?
- Tem teste A/B rodando?
- Velocidade de carregamento mobile? (Importante pra Google e SEO de Quality Score)
- Tem chat/WhatsApp como conversão? Quem atende? Tempo de resposta?
- Pra Tech: como funciona o handoff de lead pro time de vendas?
- Pra Varejo: checkout próprio ou hospedado? Quantos passos?

---

## BLOCO 6 — DORES E EXPECTATIVAS

**Objetivo:** entender o que o cliente acha que está errado e o que ele espera.

- Qual o maior incômodo com tráfego hoje? (Custo subindo, leads ruins, escala travada, criativo cansando rápido)
- Já trabalhou com gestor/agência antes? Como foi?
- Qual a expectativa pros próximos 90 dias?
- Tem alguma decisão estratégica recente que afeta tráfego? (Mudança de preço, novo produto, novo mercado)
- Tem teto de orçamento ou está aberto a escalar se ROAS justificar?

---

## BLOCO 7 — SAZONALIDADE E CONTEXTO

**Objetivo:** capturar contexto temporal que afeta decisões.

- Próximas datas importantes pro negócio nos próximos 90 dias?
- Black Friday, Natal, lançamentos planejados, eventos do setor?
- Algum mês historicamente mais fraco/forte?

---

## INDICADORES DE MATURIDADE

Use isso pra classificar o nível da operação no Dossiê.

### Iniciante
- Investe há menos de 6 meses
- Não tem pixel ou CAPI configurados corretamente
- Não acompanha CAC/LTV
- 1-3 criativos rodando, raramente substituídos
- ROAS desconhecido ou muito instável

### Intermediário
- 6-24 meses de operação
- Pixel + CAPI funcionando, GA4 configurado
- Tem noção de CAC mas LTV ainda estimado
- Produz 5-15 criativos novos por mês
- ROAS conhecido e estável dentro de uma faixa

### Avançado
- 24+ meses de operação
- Atribuição multi-touch funcionando, CAPI + offline conversions
- CAC e LTV monitorados por coorte
- Produção sistemática de criativos (15+/mês), framework de teste
- ROAS por canal/campanha/criativo, decisões data-driven
