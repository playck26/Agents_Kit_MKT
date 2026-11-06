# MANUAL DE VISTORIA COM CLAUDE IN CHROME
## Documento de conhecimento do Agente Espião Concorrente

Este manual contém os prompts mestres "tudo-em-um" que o Espião entrega ao usuário para vistoria automatizada de concorrentes via extensão Claude in Chrome. O agente da extensão executa tudo em sequência num único prompt, navegando entre Meta Ads Library, Google Ads Transparency Center, Page Transparency e site do concorrente.

---

## PRÉ-REQUISITOS (verificar com o usuário antes de mandar qualquer prompt)

Antes de o usuário rodar qualquer vistoria, confirme que:

1. ✅ Extensão Claude in Chrome instalada e logada
2. ✅ Plano pago ativo (Pro, Max, Team ou Enterprise)
3. ✅ Usuário **logado no Facebook** no Chrome (pra extensão ter acesso à Meta Ads Library sem pausa)
4. ✅ Tempo disponível: 15-30 min por concorrente para vistoria completa
5. ✅ Permissões concedidas pra extensão acessar facebook.com, adstransparency.google.com e o site do concorrente

⚠️ **Importante:** se o usuário tiver Plano Pro, o Claude in Chrome usa Haiku 4.5 (modelo mais rápido). Funciona pra coleta básica, mas pode falhar em interpretações mais sutis. Se tiver Max/Team/Enterprise, o usuário pode trocar pro Opus 4.7 nas configurações da extensão pra análise mais profunda.

---

## PROMPT MESTRE 1 — VISTORIA SOLO (1 concorrente, completa)

**Quando entregar este prompt ao usuário:**
Quando ele quer analisar 1 concorrente específico em profundidade, varrendo todas as fontes públicas.

**Tempo estimado:** 15-25 minutos
**O que ele faz:** Meta Ads Library + Page Transparency + Google Ads Transparency + site do concorrente, tudo num prompt só.

**Instrução pro usuário (entregar exatamente assim):**

> Cola o prompt abaixo na extensão Claude in Chrome. Antes de colar, **substitua os 3 campos entre colchetes** pelos dados do concorrente:
>
> - `[NOME DA EMPRESA]` → ex: "Loja Tropical"
> - `[URL DO SITE]` → ex: "https://lojatropical.com.br"
> - `[PAÍS]` → normalmente "Brasil"

```
Você vai fazer uma vistoria competitiva completa do concorrente abaixo. Siga TODOS os passos em sequência, sem pular nenhum. Ao final, entregue um relatório consolidado em formato markdown com tabelas.

CONCORRENTE A ANALISAR:
- Nome: [NOME DA EMPRESA]
- Site: [URL DO SITE]
- País de operação: [PAÍS]

==================================================
ETAPA 1 — META ADS LIBRARY
==================================================
1. Abre nova aba em https://www.facebook.com/ads/library
2. Define país como [PAÍS]
3. Categoria: "Todos os anúncios"
4. Busca por: [NOME DA EMPRESA]
5. Seleciona a página correta nas sugestões (a verificada, com selo azul, ou a com mais seguidores se não houver verificada)
6. Aguarda carregar a lista de anúncios ativos
7. Anota o número total de anúncios ativos (aparece no topo: "Resultados: X anúncios")
8. Filtra por "Plataformas: Facebook + Instagram"
9. Identifica e abre os 5 anúncios mais antigos ainda ativos (priorize os com data "Em circulação desde" mais antiga)
10. Para cada um dos 5, anote:
    - Data de início ("Em circulação desde DD/MM/AAAA")
    - Plataformas onde aparece (Facebook, Instagram, Messenger, Audience Network)
    - Tipo de mídia (estático, carrossel, vídeo)
    - Se tem botão "Ver resumo do anúncio" (sinal de múltiplas variações) — quantas variações
    - Texto principal (primary text) completo
    - Headline e descrição (se aparecerem)
    - CTA do botão (Saiba mais, Compre agora, etc.)
    - URL de destino quando se clica (landing page)

==================================================
ETAPA 2 — PAGE TRANSPARENCY
==================================================
11. Volta na página do Facebook do concorrente (acessa direto pela URL ou clica no nome da página dentro da Library)
12. Procura a seção "Transparência da Página" (geralmente lateral direita ou aba Sobre)
13. Anota:
    - Data de criação da página
    - País de gestão (onde os admins estão)
    - Histórico de mudanças de nome (se houver)
    - Número de seguidores
    - Última mudança de nome (se houver)

==================================================
ETAPA 3 — GOOGLE ADS TRANSPARENCY CENTER
==================================================
14. Abre nova aba em https://adstransparency.google.com
15. Busca por: [NOME DA EMPRESA]
16. Se aparecer o anunciante verificado (com endereço e país), clica nele. Se NÃO aparecer, pula pra Etapa 4 e anote no relatório que o concorrente não está verificado no Google.
17. Anota:
    - Localização do anunciante (cidade/país verificado)
    - Número total de anúncios ativos
    - Distribuição por formato (Search / YouTube / Display / Shopping)
    - Lista os 3 anúncios mais antigos com data de início e formato

==================================================
ETAPA 4 — SITE DO CONCORRENTE
==================================================
18. Abre nova aba em [URL DO SITE]
19. Anota:
    - Faixa de preço/ticket aparente (produto/plano destacado na home)
    - Tipo de oferta principal (assinatura mensal, produto único, e-commerce, lead form, etc.)
    - CTA principal da home
    - Existência de chat/WhatsApp visível
    - Existência de prova social (logos de clientes, depoimentos, números)
    - Tipo de site (e-commerce, landing institucional, plataforma SaaS, etc.)

==================================================
RELATÓRIO FINAL
==================================================
Agora consolide tudo no formato abaixo:

# RELATÓRIO DE VISTORIA — [NOME DA EMPRESA]

## 1. Identificação
- Nome:
- Site:
- País de operação:
- Data da vistoria: (preencha com a data de hoje)

## 2. Presença Meta Ads
- Total de anúncios ativos:
- Página verificada: (Sim/Não)
- Data de criação da página:
- Histórico de nomes:
- Seguidores:

### Top 5 anúncios mais antigos (Meta)

| # | Data início | Plataformas | Mídia | Variações | CTA | URL destino |
|---|-------------|-------------|-------|-----------|-----|-------------|
| 1 | | | | | | |
| 2 | | | | | | |
| 3 | | | | | | |
| 4 | | | | | | |
| 5 | | | | | | |

### Copies dos top 5

(transcreva o texto completo de cada um, identificando claramente qual é qual)

## 3. Presença Google Ads
- Verificado no Transparency Center: (Sim/Não)
- Localização: 
- Total de anúncios ativos:
- Distribuição por formato:
- Top 3 anúncios mais antigos: (data, formato, tipo)

## 4. Site e Oferta
- Faixa de preço aparente:
- Oferta principal:
- CTA da home:
- Conversão preferida (formulário, compra direta, WhatsApp):
- Provas sociais visíveis:

## 5. Observações livres
(qualquer coisa relevante que você notou e não cabe nas seções acima)

==================================================

IMPORTANTE:
- Se em qualquer etapa você for bloqueado por login ou CAPTCHA, pause e me avise pra resolver.
- Se algum dado não estiver disponível, escreva "Não disponível" no campo — NUNCA invente.
- Não tente acessar o gerenciador de anúncios do concorrente, conta privada ou painel administrativo. Use APENAS as fontes públicas listadas.
- Ao final, salve o relatório como texto na nossa conversa pra eu copiar.
```

**Após o usuário rodar este prompt e receber o relatório:**
- Peça pra ele copiar e colar o relatório de volta pra você (no Project Espião)
- Você analisa o material seguindo o framework de inteligência competitiva
- Aplica o playbook de inferência (Parte 4 do documento "Playbook de Coleta")
- Entrega o Relatório de Inteligência Competitiva consolidado

---

## PROMPT MESTRE 2 — VISTORIA COMPARATIVA (3-5 concorrentes em sequência)

**Quando entregar este prompt ao usuário:**
Quando ele quer comparar múltiplos concorrentes do mesmo nicho lado a lado.

**Tempo estimado:** 45-90 minutos (depende do número de concorrentes)
**O que ele faz:** roda a vistoria do Prompt 1 em todos os concorrentes em sequência e gera matriz comparativa final.

**Instrução pro usuário:**

> Cola o prompt abaixo. Antes de colar, **substitua os campos entre colchetes**. Pode listar de 3 a 5 concorrentes (mais que isso, separa em duas rodadas).

```
Você vai fazer uma vistoria competitiva COMPARATIVA dos concorrentes abaixo. Para cada um, execute a vistoria completa nas 4 fontes públicas (Meta Ads Library, Page Transparency, Google Ads Transparency, site). Ao final, gere uma matriz comparativa.

CONCORRENTES A ANALISAR (em sequência):
1. Nome: [NOME 1] | Site: [URL 1]
2. Nome: [NOME 2] | Site: [URL 2]
3. Nome: [NOME 3] | Site: [URL 3]
(adicione mais se quiser, até 5 no máximo)

PAÍS DE OPERAÇÃO: [PAÍS]

==================================================
PARA CADA CONCORRENTE, EXECUTE NESTA ORDEM:
==================================================

ETAPA A — Meta Ads Library
- Abre facebook.com/ads/library
- Define país [PAÍS], categoria "Todos os anúncios"
- Busca pelo nome
- Seleciona página correta
- Anota: total de anúncios ativos, top 3 mais antigos com data e formato
- Anota: existem múltiplas variações em algum?

ETAPA B — Page Transparency
- Acessa página do Facebook do concorrente
- Anota: data criação, país de gestão, seguidores, mudanças de nome

ETAPA C — Google Ads Transparency
- Abre adstransparency.google.com
- Busca pelo nome
- Se verificado, anota: total de anúncios, distribuição por formato
- Se NÃO verificado, anota "Não verificado"

ETAPA D — Site
- Abre o site do concorrente
- Anota: faixa de preço aparente, oferta principal, CTA da home, tipo de conversão (form/compra/WhatsApp)

==================================================
APÓS COLETAR TUDO, GERA O RELATÓRIO COMPARATIVO:
==================================================

# MATRIZ COMPARATIVA DE CONCORRENTES

## 1. Tabela Principal

| Concorrente | Anúncios Meta | Verificado Google? | Anúncios Google | Página criada em | Seguidores | Faixa preço | Oferta principal | CTA Home | Conversão preferida |
|-------------|---------------|---------------------|------------------|-------------------|------------|-------------|-------------------|----------|---------------------|
| Nome 1 | | | | | | | | | |
| Nome 2 | | | | | | | | | |
| Nome 3 | | | | | | | | | |

## 2. Detalhamento por concorrente

(repita o bloco abaixo pra cada um)

### [NOME DO CONCORRENTE]
- **Top 3 anúncios mais antigos Meta:**
  1. (data, formato, descrição rápida)
  2. ...
  3. ...
- **Distribuição Google Ads:** (Search/YouTube/Display/Shopping)
- **Site — observações:**

## 3. Padrões cruzados (observações comparativas)

Responda essas perguntas em prosa:
- Qual concorrente parece investir mais (mais anúncios ativos, mais formatos, mais tempo)?
- Há padrão dominante na faixa de preço? Algum sai da curva?
- Quais ofertas se repetem entre concorrentes?
- Quais CTAs se repetem?
- Quais formatos são dominantes no nicho?
- Algum concorrente está em mercado/segmento diferente dos outros?

==================================================

IMPORTANTE:
- Pause e me avise se encontrar login ou CAPTCHA.
- Use SOMENTE fontes públicas, nada de tentar acessar dados privados.
- Se algum dado não estiver disponível, escreva "Não disponível" — NUNCA invente.
- Vá um concorrente de cada vez, completando todas as 4 etapas (A, B, C, D) antes de partir pro próximo. Isso evita confusão de abas.
- Se o tempo estiver longo demais, salve o que já coletou parcialmente em vez de perder tudo.
```

---

## PROMPT MESTRE 3 — VISTORIA PROFUNDA DE CRIATIVOS (foco em criativo, 1 concorrente)

**Quando entregar este prompt ao usuário:**
Quando o foco é especificamente análise criativa profunda — entender hooks, copies, padrões visuais — de UM concorrente que já se sabe que é relevante.

**Tempo estimado:** 20-40 min
**O que ele faz:** mergulho profundo só na Meta Ads Library, extraindo até 15 criativos com análise detalhada.

**Instrução pro usuário:**

```
Você vai fazer uma vistoria PROFUNDA dos criativos do concorrente abaixo na Meta Ads Library. O foco é entender padrões criativos, ângulos, hooks e copies. Não precisa ir em outros sites — só Meta Ads Library.

CONCORRENTE: [NOME DA EMPRESA]
PAÍS: [PAÍS]

==================================================
EXECUÇÃO
==================================================

1. Abre facebook.com/ads/library
2. País: [PAÍS], Categoria: "Todos os anúncios"
3. Busca pelo nome, seleciona página correta
4. Aguarda carregar todos os anúncios ativos
5. Anota o total de anúncios ativos
6. Aplica filtros: Plataformas = Facebook + Instagram
7. Aplica filtro Tipo de mídia = Imagem (descarta vídeos por enquanto)
8. Identifica os 10-15 anúncios estáticos mais antigos ainda ativos
9. Para cada um, extrai detalhadamente:
   - Data de início
   - Plataformas onde aparece
   - Quantas variações tem (clica em "Ver resumo do anúncio" se aparecer)
   - Texto principal (primary text) COMPLETO, palavra por palavra
   - Headline
   - Descrição
   - Texto sobre a imagem (se houver — descreva se for texto sobreposto)
   - Descrição visual da imagem (o que está na imagem: pessoa, produto, ambiente, cor dominante)
   - CTA do botão
   - URL de destino

==================================================
APÓS COLETAR, GERA O RELATÓRIO:
==================================================

# VISTORIA PROFUNDA DE CRIATIVOS — [NOME DA EMPRESA]

## 1. Visão geral
- Total de anúncios ativos:
- Total de anúncios estáticos analisados:
- Período coberto: (anúncio mais antigo X anúncio mais recente entre os analisados)

## 2. Inventário detalhado (15 criativos)

### Criativo 1
- Data início: 
- Plataformas:
- Variações:
- Mídia: estático
- Imagem (descrição visual):
- Texto sobre imagem:
- Primary text:
"""
[copia o texto completo aqui]
"""
- Headline:
- Descrição:
- CTA:
- URL destino:

### Criativo 2
(mesmo formato)

(repete pra todos os 10-15)

## 3. Padrões criativos identificados

Responda em prosa:
- **Hooks dominantes:** que tipo de gancho aparece com mais frequência? (texto grande, rosto humano, produto isolado, antes/depois, etc.)
- **Tipos de imagem mais usados:** produto isolado, lifestyle, UGC, infográfico, comparação, etc.
- **Cores dominantes:** há paleta clara que se repete?
- **Estrutura de copy mais comum:** começa com pergunta, com afirmação, com número, com prova social?
- **Tipos de CTA:** quais aparecem mais e quais aparecem menos?
- **Ângulos identificados:** quais ângulos narrativos foram explorados? (dor → solução / autoridade / prova social / urgência / comparativo / educacional / institucional)
- **Concentração:** está apostando em pouca variação ou testando muita coisa?

## 4. Observações livres
(o que mais você notou que vale registrar)

==================================================

IMPORTANTE:
- Se você for bloqueado, pause e avise.
- Não invente nada que não viu.
- Se um anúncio tiver vídeo, pula (já dissemos que estamos focando em estáticos).
- Se o concorrente tiver menos de 10 anúncios estáticos, analisa todos os disponíveis e avisa no relatório.
- Mantenha as transcrições de copy 100% fiéis. Não parafraseie.
```

---

## REGRAS DO ESPIÃO PARA USAR ESTE MANUAL

Quando o usuário pedir vistoria de concorrentes:

### Passo 1 — Identificar a tarefa correta

O Espião pergunta:
- "Você quer analisar **1 concorrente em profundidade total** (Meta + Google + site)? → Prompt 1"
- "Você quer **comparar 3-5 concorrentes do mesmo nicho** lado a lado? → Prompt 2"
- "Você quer **mergulho profundo só nos criativos** de 1 concorrente que já é referência? → Prompt 3"

### Passo 2 — Verificar pré-requisitos

Confirma com o usuário antes de entregar o prompt:
- Extensão instalada e logada?
- Logado no Facebook no Chrome?
- Tem o nome e o site do(s) concorrente(s)?
- Tem 15-90 min disponíveis (depende do prompt)?

### Passo 3 — Entregar o prompt formatado

Entregue o prompt mestre escolhido **dentro de um bloco de código** (3 crases), com os campos entre colchetes claramente marcados pra substituir. Diga exatamente o que substituir.

### Passo 4 — Aguardar e receber o relatório

Quando o usuário voltar com o relatório gerado pela extensão, o Espião:
1. Confirma que o relatório veio completo (todas as seções preenchidas, sem [LACUNA] crítica)
2. Aplica o **Playbook de Inferência** (Parte 4 do documento "Playbook de Coleta") sobre os dados
3. Gera o **Relatório de Inteligência Competitiva** completo seguindo o template do Espião
4. Entrega com handoff pro próximo agente

### Passo 5 — Caso o usuário relate problema

Problemas comuns e como o Espião deve responder:

| Problema | Resposta |
|----------|----------|
| Extensão pediu login no Facebook | "Faça login normalmente, ela continua de onde parou" |
| Extensão pediu CAPTCHA | "Resolva o CAPTCHA, ela retoma" |
| Concorrente sem anúncios na Library | "Significa que não está rodando ads na Meta no momento. Anote como [LACUNA] e siga com Google e site" |
| Concorrente não verificado no Google Transparency | "Normal pra empresas pequenas/médias. Marque 'não verificado' e siga" |
| Bateu limite de uso da extensão | "Aguarde reset (no Pro é a cada 5h, no Max é mais flexível) ou continue manualmente" |
| Extensão travou ou demorou demais | "Cancele, abra nova conversa na extensão e rode o prompt novamente, dividindo se necessário" |

---

## DICAS PARA O USUÁRIO (incluir no que o Espião conta)

1. **Não rode 2 prompts ao mesmo tempo na extensão** — a navegação fica confusa.
2. **Mantenha o Chrome aberto e visível** durante a execução — em modo minimizado ou em background pode ficar lento.
3. **Não use o Chrome pra outras coisas** durante a vistoria — pode atrapalhar a navegação automática.
4. **Se a extensão pedir confirmação** pra alguma ação, leia antes de aceitar — sites maliciosos podem tentar prompt injection.
5. **Salve o relatório final** assim que sair — copie pra um doc no drive antes de fechar a conversa da extensão.
