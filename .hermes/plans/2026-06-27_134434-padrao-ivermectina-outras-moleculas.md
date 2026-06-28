# Padrão Ivermectina para as Outras Moléculas — Implementation Plan

> **For Hermes:** Use subagent-driven-development skill to implement this plan task-by-task.

**Goal:** transformar as outras fichas da Pharmacopeia.info no mesmo nível editorial da ivermectina: cada molécula com história/narrativa própria, imagens didáticas, oito eixos biofísicos, evidência estratificada, fontes e guardrails clínicos.

**Architecture:** usar a ficha de ivermectina como “gold standard” estrutural, não como cópia literal. Cada molécula terá um dossiê editorial próprio em `Material-Projeto/`, assets padronizados em `pharmacopeia.info/assets/moleculas/<slug>/`, e página final em `pharmacopeia.info/moleculas/<slug>/index.html`. O fluxo deve separar pesquisa, roteiro visual, geração/curadoria de imagens, implementação HTML e auditoria pré-publicação.

**Tech Stack:** static HTML/CSS/JS, imagens PNG/SVG, GitHub Pages, validação via scripts Python/grep/curl, conteúdo-fonte em Markdown no PKA.

---

## 1. Contexto atual

### 1.1. Ficha referência 100% pronta

A ficha de referência é:

```txt
pharmacopeia.info/moleculas/ivermectina/index.html
```

Elementos que definem o padrão:

1. **Hero editorial**
   - `Ficha 01 · molécula`
   - tese inicial forte: “A bula vê X. A Pharmacopeia lê Y.”
   - CTA para eixos e retorno ao atlas.

2. **Tese pública + guardrail clínico**
   - separa valor epistemológico da molécula de uso/protocolo.
   - aviso explícito: educacional, sem dose, sem prescrição.

3. **Leitura rápida em camadas**
   - 6 cards com estatutos: `estabelecido`, `hipótese biofísica`, `investigacional`, `prudência`.

4. **Figuras didáticas**
   - seção `#figuras`.
   - grid com 4 imagens editoriais GPT/OpenAI:
     - molécula / arquitetura visual.
     - mecanismo clássico.
     - mapa farmacológico.
     - interface biofísica.

5. **Matriz de 8 eixos**
   - origem.
   - arquitetura.
   - espectro/luz.
   - água/interface.
   - CISS/spin.
   - redox/mitocôndria.
   - campo/geografia/ambiente.
   - janela clínica/prudência.

6. **Evidência estratificada**
   - o que é verde/estabelecido.
   - o que é ciano/mecanístico plausível.
   - o que é âmbar/fronteira Kruse-PKA.

7. **Fontes internas e externas**
   - PKA / monografias internas.
   - história científica.
   - mecanismos farmacológicos clássicos.
   - fontes específicas de fronteira, quando existirem.

8. **Regra editorial final**
   - “perguntas melhores, não atalhos terapêuticos”.
   - distinção clara entre consenso, hipótese e fronteira investigacional.

### 1.2. Assets existentes da ivermectina

A ivermectina tem assets em:

```txt
pharmacopeia.info/assets/moleculas/ivermectina/
pharmacopeia.info/assets/moleculas/ivermectina/gpt/
```

Padrão de nomes aprovado:

```txt
<slug>-01-molecula-gpt.png
<slug>-02-<mecanismo-classico>-gpt.png
<slug>-03-mapa-farmacologico-gpt.png
<slug>-04-interface-biofisica-gpt.png
```

Para moléculas futuras, manter a mesma ordem semântica, adaptando apenas o nome do mecanismo.

### 1.3. Moléculas publicadas que precisam subir para o padrão ivermectina

Prioridade sobre as fichas já publicadas no site:

```txt
moleculas/tetraciclina/index.html
moleculas/doxiciclina/index.html
moleculas/nitrofurantoina/index.html
moleculas/lugol-5/index.html
moleculas/nac/index.html
moleculas/dmso/index.html
moleculas/dipirona/index.html
moleculas/arnica-montana/index.html
moleculas/florais-de-bach/index.html
```

Ivermectina fica fora da fila porque já é o padrão de referência.

### 1.4. Próximas candidatas ainda não publicadas ou não priorizadas

Depois de nivelar as publicadas:

```txt
tabaco-nicotina
oleo-de-ricino
benzilpenicilina
bicarbonato-de-sodio
borax-borato-de-sodio
semaglutida
metformina
rapamicina
```

---

## 2. Definição do “pacote completo” por molécula

Cada molécula só deve ser marcada como **100% pronta** quando tiver os seguintes artefatos:

```txt
Material-Projeto/padrao-ivermectina/<slug>/DOSSIER.md
Material-Projeto/padrao-ivermectina/<slug>/HISTORIA.md
Material-Projeto/padrao-ivermectina/<slug>/ROTEIRO-IMAGENS.md
Material-Projeto/padrao-ivermectina/<slug>/PROMPTS-IMAGENS.md
Material-Projeto/padrao-ivermectina/<slug>/CHECKLIST-PUBLICACAO.md
pharmacopeia.info/assets/moleculas/<slug>/gpt/<slug>-01-molecula-gpt.png
pharmacopeia.info/assets/moleculas/<slug>/gpt/<slug>-02-<mecanismo>-gpt.png
pharmacopeia.info/assets/moleculas/<slug>/gpt/<slug>-03-mapa-farmacologico-gpt.png
pharmacopeia.info/assets/moleculas/<slug>/gpt/<slug>-04-interface-biofisica-gpt.png
pharmacopeia.info/moleculas/<slug>/index.html
```

### 2.1. Conteúdo obrigatório do `DOSSIER.md`

Cada dossiê deve conter:

1. nome comum, nome técnico e slug.
2. classificação no framework: 1ª ordem, 1ª ordem condicional, 2ª ordem, investigacional, crise aguda etc.
3. monografias-fonte internas.
4. mecanismo farmacológico clássico.
5. história da descoberta/uso.
6. arquitetura molecular.
7. espectro/luz.
8. água/EZ/interface.
9. CISS/spin.
10. mitocôndria/redox.
11. campo magnético/geografia/ambiente.
12. janela clínica e riscos.
13. estatuto de evidência por afirmação.
14. frases proibidas / claims a evitar.
15. tese pública em 1 parágrafo.

### 2.2. Conteúdo obrigatório do `HISTORIA.md`

A história não é anedota solta; ela deve explicar por que a molécula existe e que tipo de ambiente a produziu.

Estrutura:

```md
# História editorial — <Molécula>

## Origem
- Quem descobriu / sintetizou / popularizou.
- Onde e quando.
- Que problema médico ou industrial ela resolvia.

## Ambiente de nascimento
- Solo, fermentação, indústria química, planta, mineral, laboratório, tradição homeopática etc.
- Se houver geografia relevante, registrar sem transformar em prova terapêutica.

## Entrada na clínica
- Para que entrou originalmente.
- Como se consolidou.
- Que usos foram abandonados ou controversos.

## Virada Pharmacopeia
- O que a bula vê.
- O que a biofísica lê.
- O que é estabelecido vs hipótese.

## Frase-mãe da ficha
“A bula vê _____. A Pharmacopeia lê _____.”
```

### 2.3. Conteúdo obrigatório do `ROTEIRO-IMAGENS.md`

Quatro imagens por molécula:

#### Imagem 01 — Molécula / arquitetura

Mostra a forma estrutural ou símbolo químico visual da molécula.

Obrigatório:
- fundo branco/off-white.
- traço limpo.
- sem cara de anúncio farmacêutico.
- sem dose, posologia ou promessa clínica.

#### Imagem 02 — Mecanismo clássico

Mostra o mecanismo aceito pela farmacologia clássica.

Exemplos:
- tetraciclina/doxiciclina: ribossomo bacteriano 30S / inibição da síntese proteica.
- nitrofurantoína: redução do grupo nitro / radicais e dano bacteriano.
- NAC: cisteína → glutationa / muco/redox.
- DMSO: solvente/carreador/transdérmico + membrana/água.
- dipirona: analgesia/antipirese/espasmólise via eixo periférico-central, sem oversimplificar.
- Lugol: iodeto/iodo → tireoide/NIS/TPO, com escala dose-farmacológica.

#### Imagem 03 — Mapa farmacológico

Mostra absorção, distribuição, barreiras, órgão-alvo, metabolismo, excreção e riscos.

Obrigatório:
- mapa visual simples.
- 4 a 6 nós no máximo.
- uma legenda de prudência.

#### Imagem 04 — Interface biofísica

Mostra luz/água/EZ/spin/mitocôndria/campo, com marcação clara de hipótese.

Obrigatório:
- não apresentar hipótese como fato.
- usar linguagem de “pergunta de pesquisa”, “interface”, “fronteira”.

### 2.4. Conteúdo obrigatório de `PROMPTS-IMAGENS.md`

Para cada imagem:

```md
## <slug>-01-molecula-gpt.png

Prompt:
...

Negative prompt / evitar:
- dose.
- comprimidos comerciais.
- marcas.
- pacientes felizes.
- antes/depois.
- claims terapêuticos.
- texto pequeno demais.

Alt text:
...

Legenda pública:
...
```

---

## 3. Priorização editorial

### Lote 1 — cromóforos/construtores de primeira ordem

Fazer primeiro porque são centrais à tese Pharmacopeia:

1. `tetraciclina`
2. `doxiciclina`
3. `nitrofurantoina`
4. `lugol-5`

Racional:
- já têm forte identidade biofísica.
- exigem distinção clara entre mecanismo clássico e leitura Kruse/PKA.
- serão páginas-pilar do atlas.

### Lote 2 — segunda ordem / desobstrução / suporte

5. `nac`
6. `dmso`
7. `dipirona`

Racional:
- precisam explicar bem “não constroem ordem sozinhas”.
- risco de parecer suplemento/protocolo se a linguagem não for precisa.

### Lote 3 — fronteira/investigacional

8. `arnica-montana`
9. `florais-de-bach`

Racional:
- exigem mais cuidado epistemológico.
- imagens devem evitar qualquer aparência de validação indevida.
- precisam de disclaimers mais fortes.

---

## 4. Plano operacional por molécula

Repetir o ciclo abaixo para cada molécula.

### Task 1: Criar diretório de trabalho editorial

**Objective:** criar a pasta de produção da molécula sem mexer ainda no site publicado.

**Files:**
- Create: `Material-Projeto/padrao-ivermectina/<slug>/DOSSIER.md`
- Create: `Material-Projeto/padrao-ivermectina/<slug>/HISTORIA.md`
- Create: `Material-Projeto/padrao-ivermectina/<slug>/ROTEIRO-IMAGENS.md`
- Create: `Material-Projeto/padrao-ivermectina/<slug>/PROMPTS-IMAGENS.md`
- Create: `Material-Projeto/padrao-ivermectina/<slug>/CHECKLIST-PUBLICACAO.md`

**Step 1:** localizar fontes internas.

Run:

```bash
cd '/home/jvmasc/PKA/Knowledge Base/04. Biofisica Farmacológica (pharmacopeia.info)'
find Monografias -iname '*<slug-ou-termo>*' -type f | sort
```

**Step 2:** registrar fontes no `DOSSIER.md`.

**Step 3:** não alterar HTML ainda.

**Verification:** os cinco arquivos existem e citam explicitamente as monografias-fonte.

---

### Task 2: Extrair a história da molécula

**Objective:** produzir a narrativa histórica que hoje só a ivermectina tem bem resolvida.

**Files:**
- Modify: `Material-Projeto/padrao-ivermectina/<slug>/HISTORIA.md`

**Step 1:** pesquisar nas monografias internas.

**Step 2:** complementar com fontes externas confiáveis quando a monografia não trouxer história suficiente.

Fontes externas aceitáveis:
- artigos de revisão.
- PubChem / DrugBank / livros-texto quando apropriado.
- Nobel/CDC/OMS/FDA/EMA quando aplicável.
- história institucional verificável.

**Step 3:** escrever a “frase-mãe”:

```txt
A bula vê ______. A Pharmacopeia lê ______.
```

**Verification:** `HISTORIA.md` contém origem, entrada clínica, virada Pharmacopeia e frase-mãe.

---

### Task 3: Produzir a matriz de evidência

**Objective:** evitar que hipótese vire claim.

**Files:**
- Modify: `Material-Projeto/padrao-ivermectina/<slug>/DOSSIER.md`

**Step 1:** criar tabela:

```md
| Afirmação | Estado | Fonte | Pode ir para público? | Linguagem pública |
|---|---|---|---|---|
| ... | estabelecido / plausível / investigacional / prudência | ... | sim/não | ... |
```

**Step 2:** classificar cada eixo:
- verde: farmacologia/história/estrutura estabelecida.
- ciano: mecanismo plausível com alguma literatura.
- âmbar: Kruse/PKA/fronteira biofísica.
- vermelho: risco, contraindicação, claim proibido.

**Verification:** nenhuma afirmação de CISS, spin, EZ, campo, deutério ou POMC deve aparecer como consenso se for hipótese.

---

### Task 4: Escrever os 8 eixos no padrão ivermectina

**Objective:** transformar o dossiê em cards publicáveis.

**Files:**
- Modify: `Material-Projeto/padrao-ivermectina/<slug>/DOSSIER.md`

**Template:**

```md
## 8 eixos — <Molécula>

### 01 · origem
Título: ...
Texto público: ...
Estado: ...

### 02 · arquitetura
Título: ...
Texto público: ...
Estado: ...

### 03 · espectro
Título: ...
Texto público: ...
Estado: ...

### 04 · água
Título: ...
Texto público: ...
Estado: ...

### 05 · CISS
Título: ...
Texto público: ...
Estado: ...

### 06 · redox
Título: ...
Texto público: ...
Estado: ...

### 07 · campo
Título: ...
Texto público: ...
Estado: ...

### 08 · janela
Título: ...
Texto público: ...
Estado: ...
```

**Verification:** cada eixo tem texto curto, estatuto epistemológico e não contém prescrição.

---

### Task 5: Criar roteiro visual e prompts

**Objective:** especificar as quatro imagens antes de gerá-las.

**Files:**
- Modify: `Material-Projeto/padrao-ivermectina/<slug>/ROTEIRO-IMAGENS.md`
- Modify: `Material-Projeto/padrao-ivermectina/<slug>/PROMPTS-IMAGENS.md`

**Step 1:** definir o mecanismo clássico da imagem 02.

**Step 2:** definir o mapa farmacológico da imagem 03.

**Step 3:** definir a interface biofísica da imagem 04.

**Step 4:** escrever alt text e legenda antes de gerar.

**Verification:** cada imagem tem prompt, negative prompt, alt text e legenda pública.

---

### Task 6: Gerar ou produzir as imagens

**Objective:** criar o conjunto visual de 4 imagens por molécula.

**Files:**
- Create directory: `pharmacopeia.info/assets/moleculas/<slug>/gpt/`
- Create:
  - `<slug>-01-molecula-gpt.png`
  - `<slug>-02-<mecanismo>-gpt.png`
  - `<slug>-03-mapa-farmacologico-gpt.png`
  - `<slug>-04-interface-biofisica-gpt.png`

**Style rules:**
- fundo branco ou off-white.
- visual de farmacologia clássica/editorial.
- sem propaganda.
- sem claims terapêuticos.
- sem logotipos comerciais.
- texto mínimo e legível.
- preferir diagrama visual a ilustração sensacionalista.

**Verification:** abrir/verificar as imagens antes de integrar no HTML; rejeitar qualquer uma que pareça anúncio, protocolo, promessa ou dose.

---

### Task 7: Atualizar HTML da ficha

**Objective:** elevar a ficha ao padrão ivermectina.

**Files:**
- Modify: `pharmacopeia.info/moleculas/<slug>/index.html`

**Step 1:** preservar título, meta description e guardrails existentes quando bons.

**Step 2:** adicionar/normalizar navegação:

```html
<a href="../../index.html#matriz">Matriz</a>
<a href="#figuras">Figuras</a>
<a href="#eixos">8 eixos</a>
<a href="#evidencia">Evidência</a>
<a href="#fontes">Fontes</a>
```

**Step 3:** inserir seção de tese pública + guardrail clínico.

**Step 4:** inserir seção `#resumo` com 6 cards de leitura rápida.

**Step 5:** inserir seção `#figuras` com as 4 imagens.

HTML base:

```html
<section id="figuras" class="shell">
  <div class="section-head">
    <div>
      <div class="kicker">Figuras didáticas</div>
      <h2>Fundo branco, traço limpo, leitura farmacológica.</h2>
    </div>
    <p>Imagens minimalistas para apoiar a ficha: arquitetura molecular, mecanismo clássico, mapa farmacológico e interface biofísica. São esquemas educacionais, não estruturas químicas completas nem protocolo clínico.</p>
  </div>
  <div class="figure-grid">
    <figure class="figure-card">
      <img src="../../assets/moleculas/<slug>/gpt/<slug>-01-molecula-gpt.png" alt="..." loading="lazy" />
      <figcaption>...</figcaption>
    </figure>
    <figure class="figure-card">
      <img src="../../assets/moleculas/<slug>/gpt/<slug>-02-<mecanismo>-gpt.png" alt="..." loading="lazy" />
      <figcaption>...</figcaption>
    </figure>
    <figure class="figure-card">
      <img src="../../assets/moleculas/<slug>/gpt/<slug>-03-mapa-farmacologico-gpt.png" alt="..." loading="lazy" />
      <figcaption>...</figcaption>
    </figure>
    <figure class="figure-card">
      <img src="../../assets/moleculas/<slug>/gpt/<slug>-04-interface-biofisica-gpt.png" alt="..." loading="lazy" />
      <figcaption>...</figcaption>
    </figure>
  </div>
</section>
```

**Step 6:** inserir seção `#eixos` com 8 cards.

**Step 7:** inserir/normalizar seção `#evidencia`.

**Step 8:** inserir/normalizar seção `#fontes`.

**Step 9:** inserir regra editorial final.

**Verification:** a página abre localmente e todos os links relativos às imagens existem.

---

### Task 8: Rodar auditoria local

**Objective:** impedir publicação quebrada.

**Files:**
- Read-only audit of `pharmacopeia.info/`

Run:

```bash
cd '/home/jvmasc/PKA/Knowledge Base/04. Biofisica Farmacológica (pharmacopeia.info)/pharmacopeia.info'
python3 - <<'PY'
from html.parser import HTMLParser
from pathlib import Path

class P(HTMLParser):
    def __init__(self):
        super().__init__()
        self.links=[]
        self.imgs=[]
        self.ids=set()
    def handle_starttag(self, tag, attrs):
        d=dict(attrs)
        if 'id' in d:
            self.ids.add(d['id'])
        if tag=='a' and d.get('href'):
            self.links.append(d['href'])
        if tag=='img' and d.get('src'):
            self.imgs.append(d['src'])

root=Path('.').resolve()
errors=[]
for f in Path('moleculas').glob('*/index.html'):
    p=P(); p.feed(f.read_text(errors='ignore'))
    base=f.parent
    for src in p.imgs:
        target=(base/src).resolve()
        if not target.exists():
            errors.append((str(f),'missing img',src))
    for h in p.links:
        if h.startswith('#') and h[1:] and h[1:] not in p.ids:
            errors.append((str(f),'broken anchor',h))
print('errors', len(errors))
for e in errors:
    print(e)
PY
```

Expected:

```txt
errors 0
```

Também rodar placeholder scan:

```bash
grep -RInE 'TODO:|PLACEHOLDER|lorem ipsum|inserir aqui|PENDENTE' -- '*.html' || true
```

Expected: nenhum resultado real.

---

### Task 9: Revisão editorial antes do commit

**Objective:** garantir que a página não virou marketing médico.

Checklist:

- [ ] “Esta página é educacional” aparece claramente.
- [ ] Não há dose, ciclo, posologia ou recomendação individual.
- [ ] Não há promessa de cura, prevenção ou tratamento.
- [ ] Hipóteses Kruse/PKA estão marcadas como hipótese/fronteira.
- [ ] Mecanismo clássico está separado da leitura biofísica.
- [ ] História da molécula não é usada como prova terapêutica.
- [ ] Imagens não têm aparência de propaganda.
- [ ] Alt text existe em todas as imagens.
- [ ] Se a molécula for investigacional/homeopática/floral, o guardrail é reforçado.

---

### Task 10: Commit por molécula

**Objective:** manter histórico limpo, uma molécula por commit.

Run:

```bash
cd '/home/jvmasc/PKA/Knowledge Base/04. Biofisica Farmacológica (pharmacopeia.info)/pharmacopeia.info'
git status --short
git add moleculas/<slug>/index.html assets/moleculas/<slug>/gpt/
git commit -m "feat: upgrade <slug> ficha to ivermectina standard"
```

Se também houver dossiês fora do repo `pharmacopeia.info/`, eles devem ser commitados no repositório/controle correspondente do PKA, se aplicável; não misturar sem verificar o escopo git.

---

## 5. Execução multiagente sugerida

Para acelerar sem perder controle editorial:

### Agente A — Pesquisa histórica e farmacológica

Entrada:
- monografias internas.
- slug da molécula.

Entrega:
- `HISTORIA.md`.
- seção clássica do `DOSSIER.md`.
- fontes externas confiáveis.

### Agente B — Matriz biofísica / oito eixos

Entrada:
- monografias internas.
- framework de ordem terapêutica.
- `HISTORIA.md`.

Entrega:
- 8 eixos.
- matriz de evidência.
- guardrails.

### Agente C — Direção de arte / prompts

Entrada:
- `DOSSIER.md`.
- `HISTORIA.md`.
- padrão visual da ivermectina.

Entrega:
- `ROTEIRO-IMAGENS.md`.
- `PROMPTS-IMAGENS.md`.
- alt text e legendas.

### Hermes — Integração e verificação

Responsável por:
- gerar/copiar imagens.
- integrar HTML.
- rodar auditoria.
- publicar apenas após aprovação.

---

## 6. Ordem de execução recomendada

### Sprint 1 — Criar padrão e fazer tetraciclina

1. Criar `Material-Projeto/padrao-ivermectina/_TEMPLATE/`.
2. Extrair CSS/HTML reutilizável da ivermectina.
3. Fazer `tetraciclina` completa.
4. Auditar.
5. Mostrar ao João para aprovação do padrão adaptado.

### Sprint 2 — Completar família tetraciclina/redox

1. `doxiciclina`.
2. `nitrofurantoina`.
3. `lugol-5`.

### Sprint 3 — Segunda ordem

1. `nac`.
2. `dmso`.
3. `dipirona`.

### Sprint 4 — Fronteira investigacional

1. `arnica-montana`.
2. `florais-de-bach`.

---

## 7. Regras editoriais inegociáveis

1. **A ivermectina é o padrão de profundidade, não o template de conteúdo.** Cada molécula precisa de história própria.
2. **Nunca esconder estatuto epistemológico.** Estabelecido, plausível, hipótese, investigacional e prudência devem estar visíveis.
3. **Sem prescrição.** Nenhuma ficha pode virar protocolo individual.
4. **Sem estética de anúncio.** Imagens devem parecer atlas farmacológico/editorial, não suplemento, bula comercial ou propaganda.
5. **Sempre preservar rastreabilidade.** Toda página deve apontar para fontes internas e externas relevantes.
6. **Uma molécula por commit.** Facilita revisão e rollback.
7. **Não publicar lote inteiro sem revisão.** Primeiro validar tetraciclina como adaptação do padrão.

---

## 8. Critério final de “100% pronta”

Uma molécula entra no mesmo patamar da ivermectina quando:

- [ ] tem história editorial própria.
- [ ] tem frase-mãe “A bula vê X; a Pharmacopeia lê Y”.
- [ ] tem 4 imagens didáticas aprovadas.
- [ ] tem seção `#figuras` integrada.
- [ ] tem 8 eixos completos.
- [ ] tem evidência estratificada.
- [ ] tem fontes internas/externas.
- [ ] tem guardrail clínico específico.
- [ ] passa auditoria de links/imagens/âncoras.
- [ ] passa placeholder scan.
- [ ] foi revisada contra claims médicos.
- [ ] está commitada e publicada.
- [ ] URL live responde `200`.

---

## 9. Primeira ação concreta recomendada

Começar por `tetraciclina`, porque é a molécula mais próxima da lógica “molécula como antena / cromóforo / luz / POMC” e vai testar melhor a transposição do padrão ivermectina.

Criar:

```txt
Material-Projeto/padrao-ivermectina/tetraciclina/DOSSIER.md
Material-Projeto/padrao-ivermectina/tetraciclina/HISTORIA.md
Material-Projeto/padrao-ivermectina/tetraciclina/ROTEIRO-IMAGENS.md
Material-Projeto/padrao-ivermectina/tetraciclina/PROMPTS-IMAGENS.md
Material-Projeto/padrao-ivermectina/tetraciclina/CHECKLIST-PUBLICACAO.md
pharmacopeia.info/assets/moleculas/tetraciclina/gpt/
```

Depois gerar as quatro imagens:

```txt
tetraciclina-01-molecula-gpt.png
tetraciclina-02-ribossomo-30s-gpt.png
tetraciclina-03-mapa-farmacologico-gpt.png
tetraciclina-04-interface-biofisica-gpt.png
```

Só depois integrar em:

```txt
pharmacopeia.info/moleculas/tetraciclina/index.html
```
