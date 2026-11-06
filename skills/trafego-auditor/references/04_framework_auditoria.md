# Framework de Auditoria — Meta Ads e Google Ads

Roteiro de diagnóstico usado pelo Agente Auditor. Siga a ordem das camadas: um problema na camada de cima (ex.: tracking quebrado) invalida a leitura das camadas de baixo.

Para cada item, registre: **Status** (✅ ok · ⚠️ atenção · ❌ problema · ❓ sem dados), **Evidência** (print, número, período) e **Impacto estimado**.

---

## Camada 0 — Pré-checagem (antes de olhar métrica)

| # | Pergunta | Por que importa |
|---|---|---|
| 0.1 | Qual é o objetivo de negócio do período? (leads, vendas, agendamentos, diagnósticos) | Define qual métrica é a "verdade" |
| 0.2 | Qual o CPA ou ROAS alvo, vindo do Dossiê? | Sem alvo não existe "bom" ou "ruim" |
| 0.3 | Qual o período analisado e houve mudança grande nele? (orçamento, oferta, sazonalidade, feriado) | Evita comparar períodos incomparáveis |
| 0.4 | A conversão medida na plataforma bate com o CRM? (diferença em %) | Se a diferença passar de ~20%, a auditoria de performance fica com ressalva |

**Regra:** se 0.4 não puder ser respondido, marque todas as conclusões de CPA/ROAS como "baseadas em dado da plataforma, não validado no CRM".

---

## Camada 1 — Conta e mensuração

### Meta Ads
- [ ] Pixel ativo e recebendo eventos nos últimos 7 dias
- [ ] API de Conversões (CAPI) ativa e com deduplicação (`event_id`) funcionando
- [ ] Qualidade da correspondência de eventos (EMQ) do evento principal — anotar a nota
- [ ] Evento otimizado é o evento de negócio (ex.: `Lead` qualificado), não um evento raso (`PageView`, clique)
- [ ] Domínio verificado e eventos priorizados
- [ ] Janela de atribuição registrada (padrão 7 dias clique / 1 dia visualização)
- [ ] Leads de formulário instantâneo chegando no CRM/WhatsApp com rastreio de origem
- [ ] Nomenclatura padronizada (campanha / conjunto / anúncio)

### Google Ads
- [ ] Tag do Google ou GA4 instalada; conversões principais marcadas como "primárias"
- [ ] Conversões otimizadas (Enhanced Conversions) ativas
- [ ] Sem conversões duplicadas (GA4 importada + tag nativa contando o mesmo evento)
- [ ] Modelo de atribuição registrado (baseado em dados ou último clique)
- [ ] Auto-tagging (gclid) ativo e preservado em redirecionamentos
- [ ] Importação de conversões offline (CRM) quando a venda acontece fora do site

### Específico Brasil
- [ ] Cliques no botão de WhatsApp medidos como conversão (e, se possível, conversa iniciada)
- [ ] Banner de cookies/LGPD não está bloqueando a tag antes do consentimento sem modo de consentimento configurado

**Se a Camada 1 tiver ❌ crítico → o primeiro achado do laudo é "corrigir mensuração antes de otimizar".**

---

## Camada 2 — Campanha

| Item | O que verificar | Sinal de problema |
|---|---|---|
| Objetivo | Objetivo da campanha = objetivo de negócio | Campanha de tráfego/engajamento cobrada como se gerasse lead |
| Orçamento | Divisão entre campanhas vs resultado de cada uma | Maior gasto na campanha de pior CPA |
| Volume para aprendizado | Meta: ~50 eventos/semana por conjunto. Google: volume suficiente para lance automático | Conjuntos eternamente em "Aprendizado limitado" |
| Estratégia de lance | Coerente com volume e maturidade | CPA desejado agressivo demais sem histórico; CPC manual sem gestão |
| Estrutura | Consolidada o bastante para a verba | Verba pulverizada em muitas campanhas pequenas |
| Funil | Existe captação + remarketing proporcionais à verba | 100% em fundo de funil com público pequeno (frequência explode) |
| Edições | Mudanças frequentes resetando aprendizado | Edições significativas várias vezes por semana |

---

## Camada 3 — Conjunto / grupo de anúncios

### Meta
- Públicos: amplo/Advantage+ vs interesses vs semelhantes vs remarketing — qual traz o melhor CPA real?
- Sobreposição de públicos entre conjuntos ativos
- Exclusões: clientes atuais e convertidos excluídos da captação
- Geografia coerente com a operação (ex.: serviço que só atende uma região)
- Posicionamentos: Advantage+ ou manual, e se algum posicionamento consome verba sem converter
- Frequência por conjunto no período

### Google
- Search: termos de pesquisa reais — % do gasto em termos irrelevantes
- Palavras-chave negativas e listas compartilhadas
- Tipos de correspondência coerentes com a estratégia de lance
- Índice de qualidade das principais palavras (e qual componente puxa para baixo)
- Parcela de impressões perdida por orçamento vs por classificação
- Performance Max: grupos de recursos, sinais de público, termos de pesquisa e exclusões de marca
- Programação e local (raio/cidades) coerentes com a operação

---

## Camada 4 — Anúncio

- Quantidade de anúncios ativos por conjunto (poucos = sem teste; muitos = verba diluída)
- Fadiga: CTR caindo e CPM/frequência subindo nas últimas 2–3 semanas
- Variedade de formatos (estático, carrossel, vídeo) e de ângulos
- Coerência anúncio → página (mesma promessa, mesma oferta)
- Recursos/extensões do Google: sitelinks, frases de destaque, imagens, local, chamada
- Conformidade: promessas com número precisam de fonte (CONAR); nada de prometer avaliação positiva no Google

> A análise profunda de criativo é da skill `trafego-analise-criativa`. Aqui registre só sinais de fadiga e incoerência e encaminhe.

---

## Camada 5 — Pós-clique

- Velocidade da página no celular (Core Web Vitals) e erros de carregamento
- Promessa da página = promessa do anúncio
- Formulário: número de campos, obrigatórios desnecessários, opção de WhatsApp
- Tempo de resposta ao lead (minutos, não horas) e quem responde
- Taxa de conversão da página e de lead → reunião/venda (dado do CRM)

> Melhorias de página são da skill `cro`; de formulário, `signup`. Encaminhe.

---

## Classificação dos achados

| Gravidade | Critério | Prazo |
|---|---|---|
| 🔴 Crítico | Desperdiça verba agora ou invalida a mensuração | 24–48h |
| 🟡 Importante | Afeta resultado de forma relevante | 1–2 semanas |
| 🟢 Otimização | Ganho incremental | Quando houver espaço |

| Tipo de correção | Exemplo |
|---|---|
| Quick win | Pausar, negativar, ajustar orçamento, corrigir configuração |
| Projeto | Novo criativo, nova página, integração de CAPI/CRM |

---

## Benchmarks: como usar

Não existe tabela universal. Use, nesta ordem:
1. **Histórico da própria conta** (mesmo período do ano anterior ou últimos 90 dias).
2. **Metas do Dossiê** (CPA/ROAS alvo calculados a partir de ticket e margem).
3. **Referências externas com fonte citada** — sempre marcadas como "referência de mercado", nunca como regra.

Se nenhuma das três existir, diga isso no laudo e proponha a meta a ser medida nas próximas 2–4 semanas.
