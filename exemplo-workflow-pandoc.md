# Exemplo Prático: Workflow Completo Markdown → Word

Este documento demonstra o workflow completo usando o protocolo CardioFit como exemplo.

---

## Passo 1: Escrever em Markdown

**Ficheiro:** `protocolo-cardiofit-rascunho.md`

Começam com rascunho simples em qualquer editor de texto:

```markdown
---
title: "CardioFit - App de Reabilitação Cardíaca"
author: "Grupo Exemplo"
date: "2026-02-28"
---

# Protocolo

## Racional

O enfarte é muito comum em Portugal...
```

**Vantagens nesta fase:**
- ✓ Foco no conteúdo, não na formatação
- ✓ Fácil de editar e iterar
- ✓ Versionável (texto simples, vê diferenças linha a linha)
- ✓ Funciona em qualquer editor

---

## Passo 2: Refinar e Estruturar

**Ficheiro:** `protocolo-cardiofit-v2-formatado.md`

Expandem o rascunho:
- Adicionar detalhes
- Criar tabelas
- Estruturar melhor
- Usar todos os recursos Markdown

```markdown
### 2.1 Desenho do Estudo

| Característica | Detalhe |
|----------------|---------|
| Randomização | 1:1 (intervenção : controlo) |
| Duração | 16 semanas |
| Setting | CHUSJ, Porto |
```

**Ainda em texto simples!**

---

## Passo 3: Converter com Pandoc

### Opção A: Pandoc Online

1. Ir para **pandoc.org/try**
2. Copiar TODO o conteúdo do ficheiro `.md`
3. Colar na caixa à esquerda
4. Configurar:
   - **from:** Markdown
   - **to:** DOCX
5. Clicar **Convert**
6. Download `output.docx`

### Opção B: Pandoc Terminal (se instalado)

```bash
pandoc protocolo-cardiofit-v2-formatado.md \
  -o protocolo-cardiofit-v2.docx \
  --toc \
  --toc-depth=3
```

**Flags opcionais:**
- `--toc`: Gera índice automático
- `--toc-depth=3`: Índice até nível 3
- `--number-sections`: Numera secções automaticamente

---

## Passo 4: Formatação em Word

Abrir `protocolo-cardiofit-v2.docx` no Word.

### 4.1 Aplicar Estilos

**Antes:** Pandoc já criou estrutura básica, mas estilos precisam de refinamento

**Fazer:**

1. **Títulos principais** (ex: "1. Introdução")
   - Selecionar → Aplicar **Título 1**
   
2. **Subtítulos** (ex: "1.1 Racional")
   - Selecionar → Aplicar **Título 2**
   
3. **Sub-subtítulos** (ex: "2.2.1 Critérios Inclusão")
   - Selecionar → Aplicar **Título 3**

**Modificar estilos** (opcional):
- Click direito no estilo → Modificar
- Alterar fonte, tamanho, espaçamento
- "Actualizar automaticamente" para aplicar globalmente

### 4.2 Inserir Índice Automático

**Posição:** Geralmente após título, antes da introdução

1. Inserir quebra de página após título
2. Posicionar cursor
3. **Referências** → **Índice** → **Índice Automático**
4. Escolher estilo (geralmente "Automático 1")

**Actualizar depois:**
- Click direito no índice → Actualizar Campo
- "Actualizar índice inteiro"

### 4.3 Cabeçalhos e Rodapés

**Cabeçalho:**
1. Duplo click na parte superior da página
2. Adicionar:
   ```
   CardioFit: Ensaio Clínico Randomizado | Grupo Exemplo
   ```
3. Alinhar à direita (opcional)
4. Marcar "Primeira página diferente" (para não ter cabeçalho na capa)

**Rodapé:**
1. Duplo click na parte inferior
2. Inserir → Número de Página → Parte Inferior → Número Simples
3. Adicionar data:
   ```
   Página X | Março 2026
   ```

### 4.4 Quebras de Página

Inserir quebras antes de secções principais:
- Antes de "1. Introdução"
- Antes de "2. Métodos"
- Antes de "3. Outcomes"

**Como:** Cursor antes do título → Insert → Page Break (Ctrl+Enter)

### 4.5 Formatação de Tabelas

Se tabelas ficarem mal formatadas:

1. Click na tabela
2. **Design de Tabela** → Escolher estilo
3. Ajustar larguras de colunas manualmente
4. Centralizar cabeçalhos (opcional)

---

## Passo 5: Guardar e Nomear

### Nomenclatura de Ficheiros

```
protocolo-cardiofit-v1.md       ← Versão 1 Markdown (fonte)
protocolo-cardiofit-v1.docx     ← Versão 1 Word (output)

protocolo-cardiofit-v2.md       ← Versão 2 Markdown (melhorada)
protocolo-cardiofit-v2.docx     ← Versão 2 Word (formatada)
```

Guardar **ambos os ficheiros** — o `.md` é a fonte que podem sempre reeditar e reconverter; o `.docx` é o que partilham e entregam.

---

## Comparação: Antes vs Depois

### ANTES (Rascunho v0.1)

```markdown
## Racional

O enfarte é muito comum em Portugal. Cerca de 12 mil casos 
por ano. Depois do enfarte, os doentes devem fazer 
reabilitação cardíaca mas muitos não fazem ou desistem.
```

**Problemas:**
- Vago ("muito comum")
- Sem números específicos de impacto
- Sem evidência sobre RC
- Sem justificação do gap

### DEPOIS (Versão Completa)

```markdown
### 1.1 Racional

O enfarte agudo do miocárdio (EAM) afecta aproximadamente 
12.000 portugueses anualmente, mantendo-se como principal 
causa de mortalidade cardiovascular. Apesar dos avanços 
terapêuticos, a taxa de reenfarte aos 5 anos permanece 
em 15-20%.

A reabilitação cardíaca (RC) baseada em exercício reduz 
a mortalidade cardiovascular em 26% e reinternamentos em 18%. 
Contudo, apenas 30-40% dos elegíveis participam em programas 
de RC, e 50% abandonam precocemente...
```

**Melhorias:**
- ✓ Dados epidemiológicos específicos
- ✓ Evidência quantificada (26%, 18%)
- ✓ Gap claro identificado
- ✓ Estrutura lógica (problema → solução → gap → este estudo)

---

## Dicas Práticas

### Markdown

**Faça:**
- ✓ Use tabelas para critérios, timelines, características
- ✓ Use listas numeradas para objetivos, passos
- ✓ Use negrito para destacar termos-chave
- ✓ Mantenha uma linha em branco entre parágrafos

**Evite:**
- ✗ Formatação manual (cores, tamanhos de fonte)
- ✗ Espaços múltiplos para alinhamento
- ✗ Caracteres especiais não-standard

### Pandoc

**Se conversão falhar:**
- Verificar metadados YAML (3 hífens antes e depois)
- Verificar sintaxe de tabelas (alinhamento `|`)
- Remover caracteres especiais problemáticos
- Testar com ficheiro mais simples primeiro

### Word

**Ordem correcta:**
1. Primeiro aplicar **estilos**
2. Depois inserir **índice**
3. Depois **cabeçalhos/rodapés**
4. Por último **ajustes finos**

Fazer nesta ordem evita ter de refazer trabalho!

---

## Checklist Final

Antes de considerar documento "completo":

- [ ] Metadados YAML presentes e correctos
- [ ] Todas as secções SPIRIT obrigatórias presentes
- [ ] Tabelas bem formatadas (alinhamento correcto)
- [ ] Critérios de inclusão/exclusão específicos e verificáveis
- [ ] Descrição detalhada da intervenção (não vaga)
- [ ] Extensão apropriada (~1200-1500 palavras para secções iniciais)
- [ ] Convertido para Word sem erros
- [ ] Estilos Título 1, 2, 3 aplicados consistentemente
- [ ] Índice automático inserido e actualizado
- [ ] Cabeçalhos/rodapés configurados *(podem fazer em casa)*
- [ ] Quebras de página antes de secções principais
- [ ] Ambos ficheiros guardados (`.md` e `.docx`)

---

**Este exemplo está disponível na pasta `exemplos/` do repositório.**

**Ficheiros incluídos:**
- `protocolo-cardiofit-rascunho.md` - Versão inicial
- `protocolo-cardiofit-v2-formatado.md` - Versão melhorada
- `protocolo-cardiofit-completo.md` - Versão final completa
