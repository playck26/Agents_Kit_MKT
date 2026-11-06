---
name: mercado-brasil
description: "Camada de adaptação ao mercado brasileiro. Use SEMPRE junto com qualquer outra skill de marketing quando o público, a empresa ou o idioma for Brasil/português — copy, e-mail, WhatsApp, SEO, preços, prospecção, CRO, conteúdo, lançamento. Também use quando o usuário mencionar 'Brasil', 'brasileiro', 'LGPD', 'WhatsApp', 'Pix', 'Reclame Aqui', 'Google Meu Negócio', 'português', 'adaptar para o Brasil' ou 'mercado nacional'. Traduz premissas americanas das outras skills (leis, canais, ferramentas, benchmarks, tom) para a realidade brasileira."
metadata:
  version: 1.0.0
---

# Mercado Brasil

As outras skills deste projeto foram escritas para o mercado americano (SaaS, inglês, CAN-SPAM, Stripe, LinkedIn/e-mail como canal principal). Esta skill é uma **camada de tradução**: aplique o método da skill original e ajuste o resultado com as regras abaixo.

Antes de tudo, leia `.agents/product-marketing.md` (contexto da empresa e dos produtos).

## 1. Idioma e tom

- Entregue tudo em **português do Brasil**, salvo pedido contrário. Nunca traduza literalmente expressões americanas ("game-changer", "crush it", "10x"): reescreva com naturalidade.
- Tom: próximo e direto, mas respeitoso. Brasileiro compra de **pessoas e relacionamento**; mostre quem está por trás (fundadores, time, cidade).
- Use "você". Evite jargão em inglês quando houver termo comum em português (use "teste grátis", "avaliações", "painel"; NPS, CX e SaaS podem ficar).
- Datas `dd/mm/aaaa`, moeda `R$ 1.234,56`, telefone `(61) 9xxxx-xxxx`.

## 2. Canais — o que muda

| Premissa americana | No Brasil |
|---|---|
| E-mail é o canal principal de nutrição e vendas | **WhatsApp** é o canal principal. E-mail é complemento (confirmações, conteúdo, propostas). |
| Formulário → SDR liga | Formulário curto → **WhatsApp em minutos**. Sempre ofereça botão de WhatsApp com mensagem pré-preenchida. |
| SMS marketing | SMS tem pouco uso em marketing; prefira WhatsApp Business API (modelos aprovados pela Meta). |
| LinkedIn como canal B2B principal | LinkedIn funciona para decisores de redes maiores; **Instagram** é forte até em B2B para PMEs e negócios físicos. |
| Reviews: G2, Capterra, Trustpilot | **Google (Perfil da Empresa)**, **Reclame Aqui** (decisivo na confiança), Capterra/B2B Stack para software. |
| Eventos: conferências SaaS dos EUA | Feiras e associações setoriais: APAS (supermercados), Abrasel (bares e restaurantes), ABF (franquias), ABRAS, eventos de CX (ex.: Consumidor Moderno). |

## 3. Leis e regras (substituem CAN-SPAM, TCPA, GDPR)

- **LGPD (Lei 13.709/2018):** toda captação precisa de base legal (consentimento ou legítimo interesse documentado), finalidade clara, link para política de privacidade e forma fácil de descadastro. Prospecção B2B fria é aceita com legítimo interesse, dados profissionais e opt-out em toda mensagem.
- **CDC (Código de Defesa do Consumidor):** oferta anunciada vincula; preço e condições devem ser claros; nada de "grátis" com cobrança escondida.
- **WhatsApp:** só envie mensagem ativa para quem deu opt-in; respeite as políticas da Meta (risco de banimento do número).
- **Google — avaliações:** é **proibido** pedir avaliação só para clientes satisfeitos (*review gating*), oferecer incentivo por avaliação ou filtrar quem recebe o link. Peça avaliação para **todos**; trate detratores em paralelo, sem bloquear o acesso ao Google.
- **CONAR:** publicidade comparativa é permitida só com dados verificáveis; números de resultado ("+70%") precisam de fonte.

## 4. Preço e pagamento

- Mostre preço em **R$**, mensal, com plano anual como desconto. Brasileiro pensa em mensalidade.
- Meios: **Pix**, boleto, cartão (parcelamento é esperado em tíquetes altos). Gateways: Asaas, Iugu, Pagar.me, Vindi, Mercado Pago, Stripe BR.
- B2B: emita **nota fiscal**; prazos de pagamento e contrato com fidelidade são comuns em redes.
- Em vez de "Free trial self-service", o padrão que converte é **diagnóstico/demonstração guiada + piloto em uma unidade**.

## 5. Ferramentas brasileiras (alternativas às citadas nas skills)

- CRM/automação: RD Station (Marketing e CRM), Ploomes, Agendor, Pipedrive, HubSpot.
- WhatsApp: Blip, Zenvia, Take, Z-API, WhatsApp Business API oficial.
- Prospecção/dados: Econodata, Speedio, Casa dos Dados (base de CNPJ), LinkedIn Sales Navigator.
- E-mail: RD Station, Brevo, E-goi, Mailchimp.

## 6. SEO no Brasil

- Pesquise palavras-chave em português e com variação regional ("cliente oculto Brasília", "pesquisa de satisfação restaurante").
- SEO local pesa muito: Perfil da Empresa no Google, páginas por cidade/segmento.
- Considere buscas no YouTube e respostas de IA (ChatGPT, Gemini, Perplexity) em português.

## 7. Benchmarks

Os números das outras skills são de mercados americanos. **Não os apresente como referência brasileira.** Quando citar números, diga a fonte ou use dados próprios do cliente. Se não houver dado, diga que é estimativa.

## 8. Checklist final (rode em toda entrega)

- [ ] Está em português natural, com R$ e formatos brasileiros?
- [ ] O WhatsApp está presente como canal/CTA?
- [ ] Cumpre LGPD (opt-in, opt-out, política) e as regras do Google para avaliações?
- [ ] Números têm fonte ou estão marcados como estimativa?
- [ ] Ferramentas e exemplos são usados no Brasil?
- [ ] Prova social é brasileira (clientes, cidades, setores locais)?
