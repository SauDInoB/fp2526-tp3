# Guia TP3 — Processamento de Texto Avançado

**Aula:** TP3 — Protocolo de Ensaio Clínico  
**Data:** 3 de Março de 2026  
**Duração:** 2 horas

---

## O Que Vamos Fazer Hoje

Hoje vão escrever as **secções iniciais do protocolo** do vosso ensaio clínico, usando IA como ferramenta de redação e Markdown como formato de trabalho:

1. Título e informação administrativa
2. Racional (introdução)
3. Objectivos
4. Desenho do estudo
5. População (critérios de elegibilidade)
6. Intervenções (descrição detalhada)

**Total:** ~1200–1500 palavras

---

## Cenários e Grupos

| Cenário | T_A | T_B | T_C |
|---------|-----|-----|-----|
| **RespiRA** (Asma) | G_1 | G_4 | G_7 |
| **MindMove** (Depressão) | G_2 | G_5 | G_8 |
| **GlucoCheck** (Diabetes T2) | G_3 | G_6 | G_9 |

**T_A:**
- G_1 · RespiRA — Matilde Ascensão, Clara Figueiras, Beatriz Martins, Rita Torres
- G_2 · MindMove — Gabriela Carneiro, Maria Leonor Fernandes, Ana Sofia Moreira, Flávio Vieira
- G_3 · GlucoCheck — José Ferreira, Diana Lopes, Rodrigo Oliveira, Tomás Santos

**T_B:**
- G_4 · RespiRA — João Paulo Cardoso, Gonçalo Cunha, Tiago Ferreira, Tiago Sousa
- G_5 · MindMove — Inês Assunção, Inês Formoso, Maria João Roldão, Maria João Roso
- G_6 · GlucoCheck — Rosarinho Barros, Mariana Dias, Luísa Moreira

**T_C:**
- G_7 · RespiRA — Rafael Batista, Mafalda Correia, Rodrigo Silva, Joana Teixeira
- G_8 · MindMove — Joana Antunes, Carlota Ferreira, Duarte Oliveira, Afonso Santos
- G_9 · GlucoCheck — João Francisco Dantas, Margarida Machado, Maria Clara Soares

---

## Workflow da Aula

```
IA + Markdown (.md) → Pandoc → Word (.docx) → Formatação final
```

### Porquê esta abordagem?

- **IA:** Acelera produção de rascunhos — mas requer revisão crítica obrigatória
- **Markdown:** Texto simples, funciona em qualquer editor, fácil de manter e partilhar
- **Pandoc:** Conversão automática para Word mantendo formatação e estrutura
- **Word:** Formatação profissional final (estilos, índices, cabeçalhos)

---

## Organização de Ficheiros

Criar uma pasta no vosso computador com esta estrutura:

```
TP3-GrupoX/
├── protocolo-v1.md      ← source Markdown (trabalham aqui)
└── protocolo-v1.docx    ← output Word (gerado pelo Pandoc)
```

- Substituir `X` pelo número do grupo (ex: `TP3-G1`)
- Guardar na Área de Trabalho ou em OneDrive
- O ficheiro `.md` é o documento de trabalho — o `.docx` é gerado a partir dele

---

## Usar IA para Redigir

### Workflow recomendado

Para cada secção do protocolo:

1. **Preparar o contexto** — ler os comentários `<!-- -->` do template para essa secção
2. **Escrever um prompt claro** — incluir cenário, PICO, secção, formato pretendido
3. **Gerar o rascunho** — com ChatGPT, Copilot, Claude, ou outro
4. **Rever criticamente** — verificar factos, especificidade, consistência com PICO
5. **Editar e integrar** — adaptar ao Markdown, corrigir, completar lacunas

### Exemplo de prompt — Racional

```
Estou a escrever o racional de um protocolo SPIRIT para um ensaio clínico randomizado.

Cenário: App móvel RespiRA para adultos com asma moderada persistente (18–65 anos).
Comparador: Cuidado habitual isolado.
Outcome primário: ACT score às 12 semanas.

Escreve um racional com ~350 palavras, estruturado em 4 parágrafos:
1. Magnitude da asma em Portugal e Europa (dados epidemiológicos específicos)
2. Limitações do cuidado habitual (baixa adesão, controlo subóptimo)
3. Evidência sobre apps móveis em asma (citar mecanismos de acção)
4. Gap específico que este estudo preenche e justificação do comparador

Usar linguagem científica formal. Texto corrido, sem marcadores de lista.
```

Adaptar o prompt ao vosso cenário (MindMove ou GlucoCheck).

### O que verificar SEMPRE após gerar

- **Números e estatísticas** — a IA inventa dados plausíveis mas frequentemente incorrectos; confirmar em PubMed, OMS, ou guidelines da área
- **Especificidade dos critérios** — ❌ "adultos" → ✅ "18–65 anos, HbA1c 7,0–9,5%"
- **Consistência com PICO** — os critérios correspondem à população definida?
- **Terminologia técnica** — GINA, PHQ-9, ACT, HbA1c — usada correctamente?
- **Descrição da intervenção** — é a vossa app específica, não uma descrição genérica
- **Nada copiado sem compreender** — se não conseguem explicar, reescrevam

### Usar IA — sim, não, talvez

| Podem usar IA para | Nunca |
|--------------------|-------|
| Gerar rascunho inicial de qualquer secção | Copiar texto sem rever |
| Sugerir estrutura de frases técnicas | Aceitar números sem verificar |
| Expandir um ponto que escreveram em lista | Ignorar inconsistências com PICO |
| Identificar lacunas no que escreveram | Substituir o vosso julgamento clínico |
| Reformular critérios de elegibilidade | Citar referências que a IA inventou |

---

## Secções a Escrever

### 1. Título (50–100 palavras)

**O que incluir:**
- Título completo e descritivo
- População, Intervenção, Comparador, Outcome
- Autores e afiliações
- Identificação do ensaio (tipo, datas)

**Exemplo:**
> "Eficácia de uma Aplicação Móvel de Monitorização de Sintomas (RespiRA) versus Cuidado Habitual no Controlo da Asma em Adultos com Asma Moderada Persistente: Um Ensaio Clínico Randomizado"

### 2. Racional (300–400 palavras)

**Estrutura sugerida:**

1. **Parágrafo 1:** Magnitude do problema
   - Dados epidemiológicos específicos
   - Impacto na saúde pública

2. **Parágrafo 2:** Limitações do cuidado actual
   - O que não funciona bem
   - Gaps na abordagem convencional

3. **Parágrafo 3:** Potencial das intervenções digitais
   - Evidência existente sobre apps na área
   - Mecanismos de acção

4. **Parágrafo 4:** Este estudo específico
   - Gap que preenche
   - Justificação da escolha do comparador
   - Relevância clínica

**Dica:** Podem usar o rascunho do TPC1 como base para o prompt. A IA expande; vocês verificam.

### 3. Objectivos (100–150 palavras)

**Dividir em:**

**Objectivo Primário:** (1 frase clara)
- Deve corresponder ao outcome primário
- Específico e mensurável

**Objectivos Secundários:** (3–5 objectivos)
- Correspondem aos outcomes secundários
- Lista ordenada por importância

**Exemplo:**
> Objectivo Primário: Avaliar a eficácia da app RespiRA na melhoria do controlo da asma, medido pelo ACT score às 12 semanas, comparado com cuidado habitual.

### 4. Desenho do Estudo (150–200 palavras)

**O que incluir:**
- Tipo de ensaio (RCT, paralelo)
- Razão de randomização (1:1)
- Duração total
- Setting (onde decorre — ex: 1 USF, 1 centro de saúde)
- Tamanho da amostra (30 participantes)
- Fases (recrutamento, baseline, intervenção, follow-up)

**Usar tabela para timeline:**

| Fase | Duração | Descrição |
|------|---------|-----------|
| Recrutamento | X semanas | ... |
| Baseline | X dias | ... |
| ... | ... | ... |

### 5. População (200–300 palavras)

**Critérios de Inclusão:**
- Cada critério deve ser **verificável**
- Ser **específico** (não vago)
- Incluir: idade, diagnóstico, critérios clínicos, capacidade tecnológica, literacia, disponibilidade

**Critérios de Exclusão:**
- Condições médicas incompatíveis
- Tratamentos concomitantes que interferem
- Gravidez/lactação (se aplicável)
- Barreiras tecnológicas

**Evitar:**
- ❌ "Adultos com diabetes" — demasiado vago
- ✅ "Adultos 40–75 anos com DM2, HbA1c 7,0–9,5%, em seguimento em CSP"

### 6. Intervenções (300–400 palavras TOTAL)

#### Grupo de Intervenção

**Descrever a app em detalhe — para cada funcionalidade:**
1. **O que faz** (descrição técnica)
2. **Como o participante interage** (experiência do utilizador)
3. **Frequência de uso esperada** (diária? semanal?)

**Incluir:** instalação e onboarding; suporte técnico; cuidado concomitante

#### Grupo Controlo

**Descrever o comparador:**
- O que exactamente recebem
- Com que frequência
- Que contactos têm com a equipa
- Justificação (porquê este comparador)

---

## Divisão de Tarefas Sugerida

| Pessoa | Secções | Palavras | Tempo |
|--------|---------|----------|-------|
| 1 | Título + Racional | ~400 | 25 min |
| 2 | Objectivos + Desenho | ~300 | 20 min |
| 3 | População (critérios) | ~250 | 20 min |
| 4 | Intervenções (ambos braços) | ~350 | 25 min |

**Depois:** juntam tudo num ficheiro único (5–10 min)

---

## Como Trabalhar em Markdown

### Sintaxe Essencial

```markdown
# Título Nível 1
## Título Nível 2
### Título Nível 3

**negrito**
*itálico*

- Item lista
- Outro item

1. Item numerado
2. Outro item

| Coluna 1 | Coluna 2 |
|----------|----------|
| Dados    | Dados    |
```

### Metadados YAML (início do ficheiro)

```markdown
---
title: "RespiRA: Ensaio Clínico Randomizado"
author: "Grupo 1 — Turma A"
date: "2026-03-03"
---
```

### Comentários (não aparecem no output)

```markdown
<!-- Isto é um comentário para vossa referência -->
```

---

## Conversão com Pandoc

### Pandoc Online (recomendado)

1. Ir para **pandoc.org/try**
2. Colar Markdown à esquerda
3. Seleccionar:
   - **from:** Markdown
   - **to:** DOCX
4. Clicar **"Convert"**
5. Download ficheiro `.docx`
6. Guardar na pasta `TP3-GrupoX/`

### Pandoc Terminal (opcional)

```bash
pandoc protocolo-v1.md -o protocolo-v1.docx
```

---

## Formatação em Word

### 1. Aplicar Estilos

**Porquê?** Consistência automática; permite criar índice; mudanças globais instantâneas.

**Como:**
1. Seleccionar título principal → Aplicar "Título 1"
2. Seleccionar subtítulos → Aplicar "Título 2"
3. Subsecções → Aplicar "Título 3"
4. Texto normal → "Normal" (geralmente já está)

### 2. Inserir Índice Automático

**Pré-requisito:** Estilos aplicados primeiro.

**Passos:**
1. Posicionar cursor onde quer o índice
2. Menu **Referências** → **Índice** → **Inserir Índice**
3. Escolher formatação → OK

**Actualizar índice:** Click direito no índice → "Actualizar Campo"

### 3. Cabeçalhos e Rodapés *(opcional — podem fazer em casa)*

**Cabeçalho:** Duplo click no topo da página → Nome do protocolo + Nome do grupo  
**Rodapé:** Duplo click no fundo → Inserir número de página

---

## Checklist Final

Antes de terminar a aula, verificar:

- [ ] Pasta `TP3-GrupoX/` criada
- [ ] Ficheiro Markdown completo com todas as secções
- [ ] Metadados YAML preenchidos
- [ ] Convertido para Word com Pandoc
- [ ] Estilos aplicados em Word
- [ ] Índice automático inserido e actualizado
- [ ] Ambos os ficheiros guardados (`protocolo-v1.md` e `protocolo-v1.docx`)

---

## Dicas

### Gestão de Tempo

- **Não percam tempo a perfeccionar** — foco em ter rascunho completo
- **Dividam tarefas** — 1 pessoa por secção
- **Usem a IA para arrancar** — é mais rápido gerar e rever do que escrever do zero
- **Juntem no final** — uma pessoa compila tudo

### Redação

- **Sejam específicos** — evitem generalizações vagas
- **Usem números** — "30 participantes", "12 semanas", "18–65 anos"
- **Tabelas ajudam** — critérios, timeline, funcionalidades
- **Consistência** — mesma informação que PICO

### Formatação

- **Estilos primeiro** — não formatar títulos manualmente
- **Índice é automático** — actualiza sozinho
- **Markdown facilita** — não se preocupem com formatação inicial

---

## TPC: Instalar Zotero + Better BibTeX

**Obrigatório antes do TP4.**

### 1. Instalar Zotero

Descarregar e instalar em [zotero.org/download](https://www.zotero.org/download/)

### 2. Instalar o plugin Better BibTeX

1. Descarregar o ficheiro `.xpi` mais recente:  
   [github.com/retorquere/zotero-better-bibtex/releases/latest](https://github.com/retorquere/zotero-better-bibtex/releases/latest)  
   *(Se usarem Firefox: click direito no link → "Guardar link como..." — não clicar directamente)*

2. No Zotero: **Tools → Plugins**

3. Clicar no ícone de engrenagem (canto superior direito) → **"Install Plugin From File..."**

4. Seleccionar o ficheiro `.xpi` descarregado → **Install**

5. Reiniciar o Zotero quando pedido

### 3. Verificar a instalação

- Ir a Zotero → **Preferences** (ou Edit → Preferences)
- O separador **"Better BibTeX"** deve aparecer
- Se aparecer: instalação bem sucedida

### 4. Opcional mas útil

Adicionar 2–3 referências à vossa biblioteca Zotero antes do TP4. Podem importar por DOI: no Zotero, clicar no botão de varinha (Add by Identifier) e colar o DOI.

---

## Próxima Aula — TP4

**Trazer:** `protocolo-v1.md` com secções iniciais + Zotero e Better BibTeX instalados.

**Primeira parte (~30 min) — Zotero + Better BibTeX:**
- Organizar a biblioteca de referências
- Citation keys: o que são, como funcionam, como configurar
- Exportar `.bib` — o ficheiro que liga as referências ao LaTeX

**Segunda parte — Introdução a LaTeX** *(colega):*
- Usar o protocolo Markdown desta aula
- Usar o `.bib` exportado para inserir citações
- Produzir documento LaTeX

---

## Recursos

- **Materiais da aula:** [saudinob.github.io/fp2526-tp3](https://saudinob.github.io/fp2526-tp3)
- **Pandoc Online:** [pandoc.org/try](https://pandoc.org/try)
- **Markdown Guide:** [markdownguide.org](https://markdownguide.org)
- **Zotero:** [zotero.org](https://www.zotero.org)
- **Better BibTeX:** [retorque.re/zotero-better-bibtex](https://retorque.re/zotero-better-bibtex/)
- **Apoio:** tiagojacinto@med.up.pt · [tiagojct.eu](https://tiagojct.eu)

---

## Erros Comuns e Como Evitar

### Erro 1: Critérios Vagos

❌ **ERRADO:**
```markdown
- Adultos com diabetes
- Sem contraindicações
- Acesso a tecnologia
```

✅ **CORRECTO:**
```markdown
- Adultos 40–75 anos com DM2, HbA1c 7,0–9,5%, em seguimento em CSP
- Sem retinopatia diabética proliferativa ou neuropatia autonómica grave
- Smartphone Android 9.0+ ou iOS 14.0+ com acesso regular à internet
```

**Porquê:** Cada critério deve ser objectivamente verificável.

### Erro 2: Descrição Vaga da Intervenção

❌ **ERRADO:**
```markdown
A app monitoriza sintomas e dá feedback ao utilizador.
```

✅ **CORRECTO:**
```markdown
A app apresenta o questionário ACT (5 itens) semanalmente às segundas-feiras,
gera gráfico de evolução do score 0–25, e envia alerta se score < 19
("Controlo inadequado — considere contactar médico").
```

**Porquê:** "Monitoriza" e "feedback" são vagos. O quê? Como? Quando?

### Erro 3: Racional Sem Estrutura

❌ **ERRADO:**
```markdown
A asma é um problema grave. Muitas pessoas têm asma. Apps podem ajudar.
Este estudo testa uma app.
```

✅ **CORRECTO:**
```markdown
[Parágrafo 1: Dados epidemiológicos específicos e verificados]
[Parágrafo 2: Limitações do cuidado actual com números]
[Parágrafo 3: Evidência sobre apps com referência]
[Parágrafo 4: Gap específico que este estudo preenche]
```

**Porquê:** Estrutura lógica, quantificação, evidência.

### Erro 4: Aceitar Dados da IA Sem Verificar

❌ **ERRADO:**
> "A asma afecta 15% da população portuguesa" *(copiado da IA sem verificar)*

✅ **CORRECTO:**
> Confirmar o número em: INE, DGS, GINA Guidelines, ou PubMed antes de usar.

**Porquê:** A IA gera dados plausíveis que podem ser incorrectos ou desactualizados.

### Erro 5: Tabelas Mal Formatadas

❌ **ERRADO:**
```markdown
| Critério | Inclusão | Exclusão
|Idade|18-65|<18,>65
```

✅ **CORRECTO:**
```markdown
| Critério | Inclusão    | Exclusão     |
|----------|-------------|--------------|
| Idade    | 18–65 anos  | < 18, > 65   |
| HbA1c    | 7,0–9,5 %   | < 7,0, > 9,5 |
```

---

## Checklist de Auto-Avaliação

### Racional

- [ ] Tem 300–400 palavras?
- [ ] Inclui dados epidemiológicos específicos verificados?
- [ ] Quantifica impacto do problema?
- [ ] Cita evidência sobre limitações do cuidado actual?
- [ ] Menciona evidência sobre potencial de apps/intervenções digitais?
- [ ] Identifica gap específico que este estudo preenche?
- [ ] Justifica escolha do comparador?

### Objectivos

- [ ] Objectivo primário é UMA frase clara?
- [ ] Corresponde ao outcome primário?
- [ ] É específico?
- [ ] Objectivos secundários são lista numerada (3–5)?
- [ ] Cada um corresponde a um outcome mensurável?

### População

- [ ] Cada critério de inclusão é verificável objectivamente?
- [ ] Idades são específicas?
- [ ] Critérios clínicos têm thresholds (ex: HbA1c 7,0–9,5%)?
- [ ] Incluiu capacidade tecnológica (tipo smartphone, SO)?
- [ ] Critérios de exclusão cobrem contraindicações médicas?

### Intervenções

- [ ] Cada funcionalidade da app está descrita em detalhe?
- [ ] Explicou COMO o participante interage?
- [ ] Especificou FREQUÊNCIA de uso esperada?
- [ ] Grupo controlo está descrito tão detalhadamente quanto intervenção?
- [ ] Justificou escolha do comparador?

### Formatação Markdown

- [ ] Metadados YAML presentes e correctos?
- [ ] Hierarquia de títulos correcta (#, ##, ###)?
- [ ] Tabelas bem formatadas (alinhamento |)?
- [ ] Negrito usado para destacar termos-chave?

---

## Recursos Externos por Cenário

### RespiRA (Asma)

- GINA Guidelines: [ginasthma.org](https://ginasthma.org)
- ACT Score: definição e thresholds (score < 20 = controlo não atingido)

### MindMove (Depressão)

- PHQ-9: scoring e interpretação (5–9 leve; 10–14 moderado)
- DSM-5: critérios diagnósticos de depressão major

### GlucoCheck (Diabetes Tipo 2)

- ADA Standards of Care: [diabetes.org](https://diabetes.org)
- HbA1c targets e interpretação clínica

### Evidência sobre Apps Móveis em Saúde

- PubMed: [pubmed.ncbi.nlm.nih.gov](https://pubmed.ncbi.nlm.nih.gov)
- Pesquisa sugerida: `[condição] AND "mobile application" AND randomized`
- Revisões Cochrane sobre mHealth na área do vosso cenário

---

## Troubleshooting Técnico

### Pandoc Online Não Funciona

**Soluções:**
1. Tentar noutro browser
2. Verificar ligação internet
3. Usar alternativa: [dillinger.io](https://dillinger.io) → Export to Word

### Tabelas Ficam Desformatadas no Word

**Soluções:**
1. Seleccionar tabela → Table Design → AutoFit → AutoFit Contents
2. Ajustar larguras manualmente (arrastar bordas)
3. Garantir que Markdown original tinha separador de cabeçalho correcto

### Estilos Não Aplicam Correctamente

**Soluções:**
1. Click direito no estilo → Modify → Alterar fonte, tamanho
2. Marcar "Update automatically"
3. Aplicar aos títulos

### Plano B: Se Pandoc Falhar Completamente

1. Copiar Markdown para Word manualmente e aplicar estilos
2. Google Docs aceita Markdown básico — converter lá, exportar para Word
3. O essencial é ter o conteúdo bem escrito em Markdown — a conversão é técnica
