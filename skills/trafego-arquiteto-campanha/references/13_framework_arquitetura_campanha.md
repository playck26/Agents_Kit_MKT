# FRAMEWORK DE ARQUITETURA DE CAMPANHA — META ADS & GOOGLE ADS
## Documento de conhecimento do Agente Arquiteto de Campanha

Este framework cobre: (1) critérios para escolher a arquitetura, (2) modelos por maturidade, (3) estruturas recomendadas para Meta Ads, (4) estruturas recomendadas para Google Ads, (5) distribuição de orçamento, (6) plano de testes e (7) regras de decisão.

---

## 1. CRITÉRIOS PARA ESCOLHER A ARQUITETURA

Antes de montar qualquer estrutura, avalie:

| Critério | Pergunta-chave | Impacto na arquitetura |
|----------|----------------|------------------------|
| Vertical | Tecnologia, Varejo ou Híbrido? | Define funil, eventos e tipo de campanha |
| Ticket | Baixo, médio ou alto? | Define janela de análise e CAC aceitável |
| Ciclo de venda | Compra rápida ou venda consultiva? | Define peso de remarketing e captura de demanda |
| Orçamento | Há verba suficiente para dividir testes? | Define quantidade de campanhas/conjuntos |
| Maturidade | Iniciante, intermediário ou avançado? | Define complexidade e automação |
| Tracking | Pixel/CAPI/GA4 confiáveis? | Define se pode otimizar para conversão final |
| Criativos | Banco forte ou raso? | Define ritmo de testes e escala |
| Oferta | Oferta validada ou em teste? | Define foco em validação ou escala |

---

## 2. MODELOS POR MATURIDADE

### 2.1 Operação Iniciante

Use quando:

- Tracking ainda não está totalmente confiável
- Conta tem pouco histórico
- Orçamento é limitado
- Oferta ou ICP ainda estão sendo validados
- Poucos criativos disponíveis

Princípios:

- Poucas campanhas
- Aprendizado concentrado
- Eventos simples e próximos do objetivo real
- Testes pequenos e controlados
- Evitar segmentação excessiva

Estrutura típica:

- 1 campanha principal de aquisição
- 1 campanha de remarketing simples, se houver volume
- 1 campanha de busca de marca no Google, se houver demanda
- 1 campanha Search genérica ou PMax enxuta, conforme o caso

### 2.2 Operação Intermediária

Use quando:

- Tracking está funcional
- Conta já tem histórico de conversões
- Orçamento permite testar sem travar aprendizado
- Existe banco mínimo de criativos
- CAC, CPA ou ROAS já são conhecidos

Princípios:

- Separar aquisição, remarketing e testes
- Criar rotina de teste criativo
- Usar públicos amplos com sinais bons
- Distribuir verba com prioridade clara
- Proteger campanhas vencedoras de testes instáveis

Estrutura típica:

- Campanha de escala/aquisição
- Campanha de testes criativos
- Campanha de remarketing
- Search de marca
- Search genérico
- PMax ou Shopping, quando aplicável

### 2.3 Operação Avançada

Use quando:

- Alto volume de conversões
- CAC/LTV medidos com consistência
- Criativos são produzidos de forma recorrente
- Tracking avançado e integrações confiáveis
- Orçamento permite isolamento de hipóteses

Princípios:

- Separar escala de experimentação
- Evitar canibalização entre campanhas
- Medir incrementalidade quando possível
- Usar automação sem perder controle estratégico
- Ter rituais claros de leitura e decisão

Estrutura típica:

- Campanhas de escala por oferta ou linha de produto
- Campanhas dedicadas de teste criativo
- Remarketing por temperatura
- Campanhas de retenção/recompra
- Search marca, genérico e concorrentes
- PMax/Shopping segmentado por margem, categoria ou prioridade

---

## 3. META ADS — MODELOS DE ARQUITETURA

### 3.1 Estrutura Enxuta

Indicada para orçamento baixo ou conta iniciante.

| Campanha | Objetivo | Público | Orçamento | Função |
|----------|----------|---------|-----------|--------|
| META_CONV_AQUISICAO_BROAD | Vendas/Leads | Broad ou Advantage+ Audience | 70-85% | Concentrar aprendizado e validar oferta |
| META_CONV_REMARKETING | Vendas/Leads | Visitantes, engajados, leads, carrinho | 15-30% | Recuperar demanda quente |

Regras:

- Se remarketing tiver pouco volume, manter dentro da campanha principal ou reduzir verba.
- Usar 3-6 criativos ativos por conjunto.
- Evitar muitos públicos pequenos.

### 3.2 Estrutura Intermediária

Indicada para conta com dados e verba moderada.

| Campanha | Objetivo | Público | Orçamento | Função |
|----------|----------|---------|-----------|--------|
| META_CONV_ESCALA_BROAD | Vendas/Leads | Broad / Advantage+ Audience | 50-65% | Escalar vencedores |
| META_CONV_TESTE_CRIATIVO | Vendas/Leads | Público amplo controlado | 15-25% | Testar ângulos e criativos |
| META_CONV_REMARKETING | Vendas/Leads | 7, 14, 30 dias conforme volume | 10-20% | Capturar intenção quente |
| META_ENG_AQUECIMENTO | Engajamento/Views | Público frio ou lookalike | 0-10% | Só usar se houver estratégia clara de topo |

Regras:

- Criativos vencedores saem da campanha de teste e entram na campanha de escala.
- Não testar público, criativo e oferta ao mesmo tempo sem controle.
- Remarketing não deve consumir verba demais se o volume de aquisição for pequeno.

### 3.3 Estrutura Avançada

Indicada para alto volume e operação madura.

| Campanha | Objetivo | Público | Orçamento | Função |
|----------|----------|---------|-----------|--------|
| META_ASC_ESCALA | Vendas | Advantage+ Shopping/Catalog ou broad | 35-50% | Escala algorítmica |
| META_CONV_ESCALA_OFERTA_[X] | Vendas/Leads | Broad ou lookalike forte | 20-35% | Escalar oferta específica |
| META_CONV_TESTE_CRIATIVO | Vendas/Leads | Público amplo padronizado | 10-20% | Isolar teste criativo |
| META_CONV_TESTE_PUBLICO | Vendas/Leads | Públicos controlados | 5-10% | Testar audiências estratégicas |
| META_CONV_REMARKETING_QUENTE | Vendas/Leads | Carrinho, checkout, lead quente | 5-15% | Fechar demanda quente |
| META_CONV_RETENCAO | Vendas/Recompra | Clientes, compradores, listas CRM | 5-15% | Recompra, upsell ou cross-sell |

Regras:

- Excluir compradores recentes quando fizer sentido.
- Controlar sobreposição entre remarketing e ASC.
- Usar janelas diferentes conforme volume e ciclo de compra.
- Proteger campanha de escala contra criativos sem validação.

---

## 4. GOOGLE ADS — MODELOS DE ARQUITETURA

### 4.1 Search de Marca

Quase sempre deve ficar separada.

| Campanha | Objetivo | Segmentação | Função |
|----------|----------|-------------|--------|
| GADS_SEARCH_MARCA | Conversão | Termos de marca | Proteger demanda existente e medir intenção direta |

Regras:

- Separar marca de genérico.
- Monitorar canibalização com PMax.
- Usar CPC baixo quando a marca já tem posição orgânica forte, salvo concorrência agressiva.

### 4.2 Search Genérico

| Campanha | Objetivo | Segmentação | Função |
|----------|----------|-------------|--------|
| GADS_SEARCH_GENERICO_[TEMA] | Leads/Vendas | Keywords por intenção | Capturar demanda ativa |

Estrutura:

- Separar grupos por intenção, não por excesso de microtemas.
- Usar phrase/exact em contas com pouco dado.
- Usar broad com smart bidding apenas quando houver conversões suficientes.
- Revisar termos de pesquisa e negativas com frequência.

### 4.3 Performance Max

| Campanha | Objetivo | Segmentação | Função |
|----------|----------|-------------|--------|
| GADS_PMAX_[OFERTA/CATEGORIA] | Vendas/Leads | Asset groups + audience signals | Escalar conversões com automação |

Regras:

- Não usar PMax como caixa preta sem assets bons.
- Separar asset groups por linha de produto, categoria, margem ou oferta.
- Controlar Final URL Expansion quando houver páginas ruins.
- Configurar exclusões de marca quando necessário.

### 4.4 Shopping para Varejo

| Campanha | Objetivo | Segmentação | Função |
|----------|----------|-------------|--------|
| GADS_SHOPPING_[CATEGORIA] | Vendas | Feed Merchant Center | Capturar demanda de produto |

Critérios de segmentação:

- Categoria
- Margem
- Ticket
- Estoque
- Prioridade comercial
- Produtos campeões vs catálogo longo

### 4.5 YouTube e Display

Use com cuidado. Normalmente entram quando:

- Há criativos adequados
- A conta já captura bem demanda existente
- Existe objetivo de topo ou remarketing
- O orçamento não prejudica Search/PMax/Meta

Funções possíveis:

- Aquecimento de público
- Remarketing visual
- Lançamento
- Educação de mercado
- Alcance com frequência controlada

---

## 5. DISTRIBUIÇÃO DE ORÇAMENTO

### 5.1 Regras gerais

- Orçamento baixo: concentrar.
- Orçamento médio: separar escala e teste.
- Orçamento alto: isolar hipóteses e proteger vencedores.
- Nunca dividir orçamento em campanhas demais se isso impedir aprendizado.
- Testes precisam de verba suficiente para gerar decisão, não só impressões.

### 5.2 Distribuição sugerida — Meta Ads

| Cenário | Aquisição/Escala | Testes | Remarketing | Retenção |
|---------|------------------|--------|-------------|----------|
| Iniciante | 70-85% | Dentro da aquisição | 15-30% | 0% |
| Intermediário | 50-65% | 15-25% | 10-20% | 0-10% |
| Avançado | 45-65% | 10-25% | 5-15% | 5-15% |

### 5.3 Distribuição sugerida — Google Ads

| Cenário | Marca | Genérico | PMax/Shopping | Remarketing/YouTube |
|---------|-------|----------|---------------|---------------------|
| Iniciante | 10-20% | 40-70% | 20-40% | 0-10% |
| Intermediário | 5-15% | 30-50% | 30-50% | 0-10% |
| Avançado | 5-10% | 25-45% | 35-60% | 5-15% |

---

## 6. EVENTOS E OTIMIZAÇÃO

### Tecnologia

Prioridade de eventos:

1. Compra/assinatura, quando houver volume
2. Oportunidade qualificada ou SQL, se integrado
3. Lead qualificado
4. Trial iniciado ou demo agendada
5. Lead bruto
6. View Content ou visita qualificada, apenas em fase inicial

Cuidados:

- Para SaaS B2B de ticket alto, nem sempre otimizar direto para venda é viável.
- Se há vendas offline, integrar CRM melhora muito a qualidade do algoritmo.
- Diferenciar lead bruto de lead qualificado evita otimização para volume ruim.

### Varejo

Prioridade de eventos:

1. Purchase
2. Initiate Checkout
3. Add to Cart
4. View Content
5. Page View, apenas em fase muito inicial

Cuidados:

- Otimizar para Add to Cart só se Purchase não tem volume.
- Separar campanhas por margem/categoria quando o ROAS agregado esconder produtos ruins.
- Feed, preço, frete e estoque impactam diretamente a arquitetura.

---

## 7. PLANO DE TESTES

Todo teste precisa ter:

- Hipótese
- Variável isolada
- Campanha/conjunto onde será testado
- Orçamento
- Duração mínima
- Métrica primária
- Regra de decisão

### Tipos de teste

| Tipo | Exemplo de hipótese | Métrica primária |
|------|---------------------|------------------|
| Criativo | Ângulo de prova social reduz CPA vs ângulo de dor | CPA / ROAS / CTR |
| Público | Broad supera interesses em CPA com mesmo criativo | CPA / volume |
| Oferta | Trial grátis converte melhor que demo consultiva | CPL qualificado / SQL |
| Landing | Página específica converte melhor que home | Taxa de conversão / CPA |
| Lance | Target CPA estabiliza custo melhor que Max Conversions | CPA / volume |

### Regras de duração

- Meta Ads: mínimo 3-7 dias, respeitando volume e aprendizado.
- Google Search: mínimo 7-14 dias, dependendo do volume de busca.
- PMax: mínimo 14-21 dias antes de conclusão forte.
- Criativo com gasto muito baixo é inconclusivo.

---

## 8. REGRAS DE DECISÃO

### Manter

Use quando:

- CPA/ROAS dentro da meta
- Volume estável
- Frequência saudável
- Tracking confiável
- Não há sinal de canibalização

### Escalar

Use quando:

- Resultado está 20-30% melhor que a meta
- Performance se mantém por pelo menos 3-7 dias
- Campanha tem espaço de público ou demanda
- Criativos não mostram fadiga

Formas de escala:

- Aumentar orçamento 15-30%
- Duplicar campanha apenas quando houver justificativa
- Levar criativo vencedor para campanha de escala
- Expandir público ou categoria

### Ajustar

Use quando:

- Métrica está próxima da meta
- Há gargalo claro em criativo, público, landing ou orçamento
- A campanha tem aprendizado útil

### Pausar

Use quando:

- Gasto suficiente sem conversão
- CPA muito acima da meta sem sinal de melhora
- Tracking confirma que o problema não é mensuração
- Criativo ou público claramente desalinhado

---

## 9. NAMING CONVENTION RECOMENDADA

Use nomes que permitam entender a estrutura sem abrir a campanha.

### Meta Ads

Formato:

`META_[OBJETIVO]_[FUNIL]_[OFERTA]_[PUBLICO]_[PAIS/REGIAO]_[DATA]`

Exemplos:

- `META_CONV_AQUISICAO_DEMO_BROAD_BR_2026-05`
- `META_CONV_TESTECRIATIVO_EBOOK_BROAD_BR_2026-05`
- `META_CONV_REMARKETING_CARRINHO_14D_BR_2026-05`

### Google Ads

Formato:

`GADS_[TIPO]_[INTENCAO/CATEGORIA]_[OFERTA]_[PAIS/REGIAO]_[DATA]`

Exemplos:

- `GADS_SEARCH_MARCA_BR_2026-05`
- `GADS_SEARCH_GENERICO_CRM_VENDAS_BR_2026-05`
- `GADS_PMAX_CATEGORIA_CALCADOS_BR_2026-05`

---

## 10. RED FLAGS DE ARQUITETURA

- Muitas campanhas com pouco orçamento.
- Teste criativo misturado com campanha de escala sem controle.
- Search de marca misturado com genérico.
- PMax canibalizando marca sem exclusão.
- Remarketing consumindo verba desproporcional ao tamanho do público.
- Otimização para evento fraco quando já existe volume para evento forte.
- Públicos muito estreitos em conta com orçamento pequeno.
- Lookalike baseado em tráfego ruim, não em compradores/leads qualificados.
- Campanhas rodando com objetivos incompatíveis com a meta real.
- Estrutura impossível de ler por falta de naming convention.

