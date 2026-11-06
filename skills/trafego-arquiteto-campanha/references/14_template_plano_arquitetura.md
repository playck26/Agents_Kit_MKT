# TEMPLATE — PLANO DE ARQUITETURA DE CAMPANHA
## Documento de conhecimento do Agente Arquiteto de Campanha

Este é o formato exato que o agente deve gerar ao final da arquitetura. Não inventar seções novas. Marcar **[LACUNA — preencher]** quando faltar informação.

---

# PLANO DE ARQUITETURA DE CAMPANHA — [Nome do Cliente]

**Data:** [DD/MM/AAAA]  
**Vertical:** [Tecnologia / Varejo / Híbrido]  
**Maturidade da operação:** [Iniciante / Intermediário / Avançado]  
**Plataformas:** [Meta / Google / Ambas]  
**Orçamento mensal total:** [R$X ou LACUNA]  
**Objetivo principal 30-90 dias:** [Leads / Vendas / ROAS / Escala / Validação / Lançamento / Outro]

---

## 1. CONTEXTO RECEBIDO

### Materiais usados

- **Dossiê do Cliente:** [Recebido / Não recebido / Parcial]
- **Laudo de Auditoria:** [Recebido / Não recebido / Parcial]
- **Laudo de Análise Criativa:** [Recebido / Não recebido / Parcial]
- **Outros dados relevantes:** [prints, CSVs, orçamento, metas, restrições]

### Síntese do cenário

[5-7 linhas em prosa resumindo o negócio, objetivo, restrições, maturidade e principal desafio estrutural.]

---

## 2. DIAGNÓSTICO ESTRUTURAL

| Área | Diagnóstico | Implicação para a arquitetura |
|------|-------------|-------------------------------|
| Oferta | | |
| Público/ICP | | |
| Tracking | | |
| Criativos | | |
| Orçamento | | |
| Funil/pós-clique | | |
| Histórico de campanha | | |

### Tipo de arquitetura recomendada

**Arquitetura:** [Enxuta / Intermediária / Avançada]

**Justificativa:** [1-3 linhas explicando por que esse nível de complexidade faz sentido.]

---

## 3. ARQUITETURA META ADS

> Se Meta Ads não fizer parte do escopo, preencher: **Não aplicável neste plano.**

### Visão geral de orçamento — Meta

**Orçamento mensal Meta:** [R$X]  
**Orçamento diário estimado:** [R$X/dia]

| Frente | % do orçamento | Valor mensal | Função |
|--------|----------------|--------------|--------|
| Aquisição/Escala | | | |
| Testes | | | |
| Remarketing | | | |
| Retenção/Recompra | | | |

### Estrutura de campanhas — Meta

| Campanha | Objetivo | Evento de otimização | Público | Orçamento | Função |
|----------|----------|----------------------|---------|-----------|--------|
| [Nome da campanha] | | | | | |
| [Nome da campanha] | | | | | |
| [Nome da campanha] | | | | | |

### Detalhamento por campanha — Meta

#### Campanha 1 — [Nome]

- **Objetivo:** 
- **Função no funil:** 
- **Evento de otimização:** 
- **Estratégia de orçamento:** [CBO/ABO/Advantage Campaign Budget]
- **Público:** 
- **Exclusões:** 
- **Posicionamentos:** 
- **Criativos/ângulos recomendados:** 
- **Orçamento inicial:** 
- **Critério para manter:** 
- **Critério para escalar:** 
- **Critério para ajustar ou pausar:** 

#### Campanha 2 — [Nome]

[Repetir estrutura]

---

## 4. ARQUITETURA GOOGLE ADS

> Se Google Ads não fizer parte do escopo, preencher: **Não aplicável neste plano.**

### Visão geral de orçamento — Google

**Orçamento mensal Google:** [R$X]  
**Orçamento diário estimado:** [R$X/dia]

| Frente | % do orçamento | Valor mensal | Função |
|--------|----------------|--------------|--------|
| Search Marca | | | |
| Search Genérico | | | |
| Performance Max / Shopping | | | |
| YouTube / Display / Remarketing | | | |

### Estrutura de campanhas — Google

| Campanha | Tipo | Estratégia de lance | Segmentação | Orçamento | Função |
|----------|------|---------------------|--------------|-----------|--------|
| [Nome da campanha] | | | | | |
| [Nome da campanha] | | | | | |
| [Nome da campanha] | | | | | |

### Detalhamento por campanha — Google

#### Campanha 1 — [Nome]

- **Tipo:** [Search / PMax / Shopping / YouTube / Display]
- **Objetivo:** 
- **Conversão principal:** 
- **Estratégia de lance:** 
- **Segmentação:** 
- **Palavras-chave / temas / asset groups:** 
- **Negativas ou exclusões necessárias:** 
- **Assets necessários:** 
- **Orçamento inicial:** 
- **Critério para manter:** 
- **Critério para escalar:** 
- **Critério para ajustar ou pausar:** 

#### Campanha 2 — [Nome]

[Repetir estrutura]

---

## 5. INTEGRAÇÃO ENTRE META E GOOGLE

[Preencher quando ambas as plataformas fizerem parte do plano.]

| Plataforma | Papel no funil | Métrica principal | Observações |
|------------|----------------|------------------|-------------|
| Meta Ads | | | |
| Google Ads | | | |

### Lógica de distribuição

[Explique como o orçamento se divide entre geração de demanda, captura de demanda, remarketing e escala.]

### Riscos de canibalização

[Liste possíveis conflitos: PMax vs Search de marca, remarketing duplicado, públicos quentes em várias campanhas, etc.]

---

## 6. PLANO DE TESTES PRIORIZADOS

### Prioridade Alta

| Teste | Hipótese | Onde testar | Duração mínima | Métrica primária | Regra de decisão |
|-------|----------|-------------|----------------|------------------|------------------|
| 1 | | | | | |
| 2 | | | | | |

### Prioridade Média

| Teste | Hipótese | Onde testar | Duração mínima | Métrica primária | Regra de decisão |
|-------|----------|-------------|----------------|------------------|------------------|
| 1 | | | | | |
| 2 | | | | | |

### Otimizações pontuais

| Ajuste | Onde aplicar | Impacto esperado |
|--------|--------------|------------------|
| 1 | | |
| 2 | | |

---

## 7. REGRAS DE GESTÃO E DECISÃO

### Rotina de leitura

- **Diária:** [o que olhar]
- **2-3x por semana:** [o que ajustar]
- **Semanal:** [decisões estruturais]
- **Mensal:** [revisão de arquitetura]

### Regras de escala

[Ex: aumentar orçamento 15-30% quando CPA ficar X% abaixo da meta por Y dias.]

### Regras de pausa

[Ex: pausar criativo/conjunto/campanha quando gastar X vezes o CPA alvo sem conversão.]

### Regras de migração

[Quando mover criativo vencedor de teste para escala, quando separar campanha, quando consolidar.]

---

## 8. NAMING CONVENTION

### Meta Ads

**Formato recomendado:**  
`META_[OBJETIVO]_[FUNIL]_[OFERTA]_[PUBLICO]_[REGIAO]_[DATA]`

**Campanhas sugeridas já nomeadas:**

1. `[Nome final da campanha]`
2. `[Nome final da campanha]`
3. `[Nome final da campanha]`

### Google Ads

**Formato recomendado:**  
`GADS_[TIPO]_[INTENCAO/CATEGORIA]_[OFERTA]_[REGIAO]_[DATA]`

**Campanhas sugeridas já nomeadas:**

1. `[Nome final da campanha]`
2. `[Nome final da campanha]`
3. `[Nome final da campanha]`

---

## 9. PRÉ-REQUISITOS ANTES DE IMPLEMENTAR

[Lista do que precisa estar pronto antes de subir ou reestruturar campanhas.]

- [ ] Tracking validado
- [ ] Eventos corretos configurados
- [ ] Conversões principais definidas
- [ ] Criativos mínimos disponíveis
- [ ] Landing/destino validado
- [ ] Orçamento aprovado
- [ ] Naming convention aprovada
- [ ] Acessos necessários disponíveis

---

## 10. LACUNAS E RISCOS

### Lacunas

- **[LACUNA]** — [por que importa]
- **[LACUNA]** — [por que importa]

### Riscos

- **[Risco]** — [impacto provável e como mitigar]
- **[Risco]** — [impacto provável e como mitigar]

---

## 11. RECOMENDAÇÃO DE PRÓXIMO AGENTE

**Próximo agente recomendado:** [Espião Concorrente / Plano de Ação / Análise Criativa / Auditor de Campanha]

**Justificativa:** [2-3 linhas explicando por que esse é o próximo passo mais lógico.]

---

## 12. 📤 PRÓXIMO PASSO

Recomendo acionar agora o **[Nome do Agente]** porque [justificativa de 1-2 linhas].

**Como fazer:**

1. Abra o Project "[Nome do Project]" no Claude
2. Inicie uma nova conversa
3. Copie o bloco abaixo e cole como primeira mensagem:

```markdown
Segue o Plano de Arquitetura de Campanha gerado pelo Agente Arquiteto de Campanha.

Modo de trabalho esperado: [Enxuto / Completo]

---

# PLANO DE ARQUITETURA DE CAMPANHA — [Nome real do cliente]

**Data:** [DD/MM/AAAA]
**Vertical:** [Tecnologia / Varejo / Híbrido]
**Maturidade da operação:** [Iniciante / Intermediário / Avançado]
**Plataformas:** [Meta / Google / Ambas]
**Orçamento mensal total:** [R$X]
**Objetivo principal 30-90 dias:** [objetivo real]

[CONTEÚDO COMPLETO DO PLANO PREENCHIDO COM DADOS REAIS]

---

Pode começar o trabalho usando esta arquitetura como base.
```

> Lembrete crítico ao agente: dentro do bloco de código acima, NÃO use placeholders. Preencha com o conteúdo real do plano gerado nesta conversa.

