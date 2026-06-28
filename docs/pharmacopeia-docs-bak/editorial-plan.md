# Plano Editorial — Pharmacopeia.info

Data: 2026-06-18
Responsável operacional: Rubem / PKA
Repo GitHub: `jvmasc/pharmacopeia.info`
Site: Pharmacopeia.info
Fonte primária interna: `Knowledge Base/Biofísica Farmacológica/`

---

## 1. Estado encontrado

### GitHub / site

- Repositório público: `jvmasc/pharmacopeia.info`.
- Estrutura atual: MVP estático em HTML/CSS/JS, publicado via GitHub Pages.
- Ficha já publicada: `moleculas/ivermectina/index.html`.
- Home atual já lista: Ivermectina, DMSO, Dipirona, Óleo de Rícino, Lítio/GLP-1 e um item sensível/interno.
- Há alterações locais não commitadas na ficha de ivermectina e assets/imagens de ivermectina. Não mexer nelas antes de decidir se entram no próximo commit.

### Team INBOX

- Verificação atual: nenhum ficheiro pendente fora de `Team INBOX/Processed/`.
- Portanto, o plano abaixo usa notas já consolidadas na Knowledge Base e Owner_s INBOX, sem processar Team INBOX.

---

## 2. Princípio editorial central

A ordem editorial deve seguir a própria hierarquia do framework:

1. **Drogas / moléculas de primeira ordem** — ferramentas que constroem ordem diretamente: CISS, POMC, melanina, OxFos, DDW endógena, estado tripleto, corrente DC de baixa entropia, reorganização estrutural.
2. **Drogas / moléculas de segunda ordem** — ferramentas que removem obstáculos: ROS, febre, espasmo, inflamação, fibrose fascial, ruído vagal-entérico, degradação de EZ, obstáculos à construção.
3. **Candidatas e fronteiras** — moléculas ainda não classificadas, hipóteses em aberto e peças de pesquisa.

Frase editorial-guia:

> Primeiro explicamos o que constrói ordem. Depois explicamos o que limpa o terreno para a ordem acontecer.

---

## 3. Cabal editorial recomendado

Objetivo: transformar as notas PKA em uma farmacopeia pública, bonita, rastreável, educacional e juridicamente defensável.

Agentes envolvidos:

- **Cláudia Mares** — linha editorial, clareza pública, SEO e tom.
- **Dra. Ana Compliance** — evitar linguagem prescritiva, promessas terapêuticas e risco regulatório.
- **Peter Picolin** — ponte clínica: o que pode ser dito como educação vs. protocolo individual.
- **Vasco** — arquitetura do site, templates HTML, cards, navegação e publicação GitHub Pages.

Ponto de contato: Rubem.
Critério de conclusão: backlog editorial aprovado + primeira leva de fichas publicáveis convertida em HTML.

---

## 4. Ordem editorial das fichas

## Fase 1 — Primeira ordem: moléculas construtoras

### 1. Ivermectina — já publicada, deve virar o padrão visual

Status: publicada.
Caminho site: `moleculas/ivermectina/`.
Fonte PKA:

- `Knowledge Base/Biofísica Farmacológica/Biofisica da Ivermectina - Framework Jack Kruse.md`
- `Framework-Ordem-Terapeutica.md`

Tese editorial:

- Lactona macrocíclica como filtro de spin mecânico-conformacional.
- Restauração de OxFos.
- Limpeza parasitária como condição para construção posterior.
- No framework, aparece na seção de primeira ordem, mas opera também como limpeza inicial em sequências terapêuticas.

Função no site:

- Peça inaugural e modelo de ficha.
- Deve estabelecer a gramática visual: molécula, mecanismo oficial, leitura biofísica, eixo luz/água/magnetismo, janela clínica, limites e disclaimers.

Ação sugerida:

- Revisar a ficha atual contra o template final.
- Marcar como `Primeira ordem / restauração OxFos / limpeza estrutural`.
- Manter disclaimer forte: educacional, não prescritivo.

---

### 2. Tetraciclina — antena fotônica de resgate agudo

Status: nota PKA pronta.
Fonte PKA:

- `Biofisica-Tetraciclina-2026-05-23.md`
- `Protocolo-Nubio-Tetraciclina-Doxiciclina-v2-2026-05-23.md`
- `Framework-Ordem-Terapeutica.md`

Tese editorial:

- Antena fotônica proteobacteriana de primeira geração.
- Núcleo de quatro anéis conjugados absorvendo UV-A.
- Estado tripleto → POMC → α-MSH → eumelanina → CISS.
- Uso conceitual como primer/resgate rápido, não como protocolo público.

Função no site:

- Primeira explicação didática de “molécula como antena”.
- Comparar medicina convencional (“antibiótico 30S”) com leitura biofísica (“antena UV-A / melanina / spin”).

Slug sugerido:

- `moleculas/tetraciclina/`

---

### 3. Doxiciclina — construção profunda e neuromelanina

Status: nota PKA pronta.
Fonte PKA:

- `Biofisica-Doxiciclina-2026-05-23.md`
- `Protocolo-Nubio-Tetraciclina-Doxiciclina-v2-2026-05-23.md`
- `Framework-Ordem-Terapeutica.md`

Tese editorial:

- Versão lipofílica e sustentada da antena tetraciclínica.
- Compartimento dérmico profundo, bainhas lipídicas, DHA, APOE, neuromelanina.
- Ciclos longos e proteção neurológica aparecem nas notas, mas a página pública deve manter linguagem educacional, não protocolar.

Função no site:

- Peça-mestre da primeira ordem: “construção sustentada”.
- Deve ficar imediatamente depois da tetraciclina para mostrar continuidade: primer superficial → construção profunda.

Slug sugerido:

- `moleculas/doxiciclina/`

---

### 4. Tabaco / Nicotina — primeira ordem condicional

Status: nota PKA pronta.
Fonte PKA:

- `Biofisica-Tabaco-2026-05-26.md`
- `Revisao-Clinica-Tabaco-PeterPicolin-2026-05-26.md`
- `Framework-Ordem-Terapeutica.md`

Tese editorial:

- Nicotina como antena quiral bicíclica e modulador vagal/POMC.
- Opera como primeira ordem apenas sob condições ambientais específicas: sol real, campo robusto, ausência de nnEMF, ritualidade, não compulsão.
- Precisa separar nicotina/plantas/protocolos tradicionais de cigarro industrial.

Função no site:

- Página de fronteira: mostra que “primeira ordem” não significa “sempre bom”.
- Excelente para ensinar dependência de contexto: molécula + ambiente + campo + forma de uso.

Risco:

- Alto risco interpretativo. Exigir revisão de Dra. Ana e Peter antes de publicação.

Slug sugerido:

- `moleculas/nicotina/` ou `moleculas/tabaco-nicotina/`

---

## Fase 2 — Segunda ordem: desobstruidores e preparadores de terreno

### 5. DMSO — segunda ordem estrutural / reorganizador de substrato

Status: nota PKA pronta.
Fonte PKA:

- `Biofisica-DMSO-2026-05-23.md`
- `Framework-Ordem-Terapeutica.md`

Tese editorial:

- Não é antena UV-A; é reorganizador de água e carreador transdérmico.
- Expulsa D+ de shells de hidratação por KIE, protege EZ, remove OH·, dissolve fibrose fascial.
- Potencializa as moléculas de primeira ordem ao preparar o substrato.

Função no site:

- Abrir a fase de segunda ordem porque é a mais importante como ponte entre limpeza e construção.
- Página deve deixar cristalino: DMSO não substitui doxiciclina/tetraciclina; prepara terreno.

Slug sugerido:

- `moleculas/dmso/`

---

### 6. Arnica Montana 6ch — segunda ordem de campo / POMC desbloqueado

Status: nota PKA pronta.
Fonte PKA:

- `Biofisica-Arnica-Montana-6ch-2026-05-25.md`
- `Protocolo-Florais-Bach-AAS-2026-05-25.md`
- `Framework-Ordem-Terapeutica.md`

Tese editorial:

- Ferramenta de segunda ordem de baixa entropia contínua.
- Atua como desbloqueio de POMC via NF-κB e reorganização de EZ water por informação de campo quiral.
- Não constrói melanina; remove freio.

Função no site:

- Introduzir uma camada mais sutil do framework sem cair em alegação homeopática vulgar.
- Deve ser publicada depois de DMSO para o leitor já entender “preparar substrato”.

Risco:

- Alto risco epistemológico. Exigir linguagem: hipótese biofísica interna / framework, não consenso médico.

Slug sugerido:

- `moleculas/arnica-montana-6ch/`

---

### 7. Florais de Bach — segunda ordem vagal-entérica

Status: nota PKA pronta.
Fonte PKA:

- `Biofisica-Florais-De-Bach-2026-05-25.md`
- `Protocolo-Florais-Bach-AAS-2026-05-25.md`
- `Framework-Ordem-Terapeutica.md`

Tese editorial:

- Desbloqueio do tônus vagal-entérico por redução de ruído de campo no plexo entérico.
- Requer coerência mínima do receptor biológico; não é fundação.
- Não substitui sol, aterramento, água ou moléculas de primeira ordem.

Função no site:

- Página de “camada de sinal”, não de “substância farmacológica clássica”.
- Boa para explicar receptor/substrato: sinais sutis falham quando o sistema está abaixo do limiar de coerência.

Risco:

- Muito alto para público externo. Pode ficar como “rascunho interno” até a linha editorial amadurecer.

Slug sugerido:

- `moleculas/florais-de-bach/`

---

### 8. Dipirona — segunda ordem de crise aguda

Status: nota PKA pronta.
Fonte PKA:

- `Biofisica-Dipirona-Monohidratado-2026-05-23.md`
- `Framework-Ordem-Terapeutica.md`

Tese editorial:

- Ferramenta hidrofílica de interface EZ/bulk.
- Remove obstáculos agudos: febre, espasmo, dor intensa, alarme simpático.
- Não constrói CISS, não ativa POMC diretamente, não gera melanina.

Função no site:

- Página crítica para o público brasileiro: molécula culturalmente comum, mas reposicionada como ferramenta de segunda ordem.
- Deve deixar claro: utilidade pontual ≠ solução estrutural.

Risco:

- Alto por ser medicamento de uso amplo. Linguagem não prescritiva obrigatória.

Slug sugerido:

- `moleculas/dipirona/`

---

### 9. Óleo de Rícino — suporte de superfície / segunda ordem fraca

Status: nota PKA pronta.
Fonte PKA:

- `Biofisica-Oleo-de-Ricino-2026-06-02.md`
- `INDEX.md`

Tese editorial:

- Ácido ricinoleico é opticamente inerte na janela solar biologicamente ativa.
- Singularidade concreta: viscosidade, emoliência, EP3 oral e possível OH-12 como sítio adicional de nucleação de EZ.
- Compressa opera principalmente por termoterapia parassimpática, reflexo cutâneo-visceral e ritual de baixa entropia.

Função no site:

- Página exemplar de honestidade epistemológica: separar real, plausível, especulativo e marketing.
- Deve ser posicionada depois de DMSO/Dipirona para não parecer “droga principal”.

Slug sugerido:

- `moleculas/oleo-de-ricino/`

---

## Fase 3 — Candidatas prioritárias futuras

Estas entram depois da base primeira/segunda ordem estar publicada.

### 10. Azul de Metileno

Fonte atual:

- `Framework-Ordem-Terapeutica.md`, seção “Moléculas Candidatas a Análise Futura”.

Hipótese:

- Forte candidato a primeira ordem por absorção ~668 nm e papel na cadeia respiratória / OxFos.

Prioridade:

- Alta. Peça excelente para conectar fotobiomodulação, mitocôndria e medicina convencional.

---

### 11. Semaglutida / Ozempic / GLP-1

Fonte atual:

- `POST-07-ozempic-biofisica-quantica-deuterio.md` em social-media specs.
- `Framework-Ordem-Terapeutica.md`.

Hipótese:

- Candidata forte por obesidade/deutério, glucagão-POMC-melanina, sinalização metabólica e mercado contemporâneo.

Prioridade:

- Alta para audiência, mas só depois de template e compliance amadurecidos.

---

### 12. Metformina

Hipótese:

- Candidata ambígua: segunda ordem por inibição do complexo I e desaceleração do pool cinético; possível primeira ordem via AMPK/k=160.

Prioridade:

- Média-alta.

---

### 13. Rapamicina / Sirolimus

Hipótese:

- mTOR, pool de replicação cinética, permanência temporal estrutural.

Prioridade:

- Média, mais técnica.

---

### 14. NAC

Hipótese:

- Provável segunda ordem: antioxidante / glutationa / modulação de ROS e possivelmente EZ via tiois.

Prioridade:

- Média.

---

## 5. Template editorial de cada ficha

Cada página deve seguir sempre a mesma matriz:

1. **Identidade da molécula**
   - Nome, classe, estrutura, origem, status regulatório/genérico.

2. **Tese em uma frase**
   - Ex.: “A doxiciclina é uma antena fotônica lipofílica que transforma UV-A em sinal POMC profundo.”

3. **O mecanismo oficial**
   - Como a farmacologia convencional explica.

4. **A leitura biofísica**
   - Luz, água, deutério, spin, CISS, membrana, mitocôndria, campo.

5. **Classificação de ordem**
   - Primeira ordem, segunda ordem ou condicional.
   - Justificar com critério de Landauer: constrói ordem ou remove obstáculo?

6. **Condição de operação**
   - Luz, campo, água, nnEMF, geografia, horário, substrato biológico.

7. **Janela clínica / educacional**
   - Nunca como prescrição; sempre como contexto de leitura.

8. **Limites e riscos**
   - O que a molécula não faz.
   - Contraindicações gerais e necessidade de profissional de saúde.

9. **Sequenciamento**
   - Antes/depois de quais moléculas; sinergias; o que não combinar.

10. **Fontes internas PKA**
   - Caminho das notas usadas.

11. **Referências externas**
   - PubMed / FDA / literatura base quando houver.

---

## 6. Arquitetura de navegação do site

### Home

A home deve deixar de ser só vitrine de cards e virar mapa editorial:

- Bloco 1: “O que é uma droga de primeira ordem?”
- Bloco 2: “O que é uma droga de segunda ordem?”
- Bloco 3: Cards em duas prateleiras:
  - Primeira ordem
  - Segunda ordem
- Bloco 4: Candidatas / em estudo
- Bloco 5: Disclaimer educacional.

### URL sugerida

- `/moleculas/ivermectina/`
- `/moleculas/tetraciclina/`
- `/moleculas/doxiciclina/`
- `/moleculas/tabaco-nicotina/`
- `/moleculas/dmso/`
- `/moleculas/arnica-montana-6ch/`
- `/moleculas/florais-de-bach/`
- `/moleculas/dipirona/`
- `/moleculas/oleo-de-ricino/`

### Campos de metadados internos por ficha

- `title`
- `slug`
- `ordem`: `primeira`, `segunda`, `condicional`, `candidata`
- `status`: `publicada`, `rascunho`, `revisao-clinica`, `revisao-compliance`
- `fontes_pka`
- `risco_publicacao`: `baixo`, `medio`, `alto`
- `revisor_clinico`
- `revisor_compliance`

---

## 7. Backlog prático de execução

### Sprint 1 — Reorganizar fundação editorial

1. Criar no repo um ficheiro editorial interno:
   - `EDITORIAL_PLAN.md` ou `docs/editorial-plan.md`.
2. Atualizar a home para separar cards em:
   - Primeira ordem
   - Segunda ordem
   - Candidatas
3. Revisar a ficha de ivermectina para virar template oficial.
4. Não mexer nas alterações locais de imagens/ivermectina sem antes decidir se entram no commit.

### Sprint 2 — Publicar primeira ordem completa

1. Tetraciclina.
2. Doxiciclina.
3. Tabaco/Nicotina como rascunho ou página “condicional / em revisão”.
4. Revisão Peter + Dra. Ana antes de tornar tabaco/nicotina pública.

### Sprint 3 — Publicar segunda ordem forte

1. DMSO.
2. Dipirona.
3. Óleo de Rícino.

### Sprint 4 — Segunda ordem sutil / alto risco epistemológico

1. Arnica Montana 6ch.
2. Florais de Bach.
3. Deixar como páginas com badge explícito: “framework biofísico / hipótese operacional”.

### Sprint 5 — Candidatas de alto impacto

1. Azul de Metileno.
2. Semaglutida / Ozempic.
3. Metformina.
4. Rapamicina.
5. NAC.

---

## 8. Regra de ouro de publicação

Nenhuma página deve parecer protocolo de uso.

A fórmula correta é:

> Esta ficha explica uma hipótese biofísica educacional sobre a molécula e seu lugar em uma hierarquia de ordem/desobstrução. Não indica dose, frequência, via de administração nem substitui avaliação clínica.

---

## 9. Próxima ação recomendada

Começar por uma alteração pequena e segura no GitHub:

1. Criar `docs/editorial-plan.md` no repo com este plano sintetizado.
2. Atualizar a seção de cards da home para refletir a hierarquia:
   - Primeira ordem: Ivermectina, Tetraciclina, Doxiciclina, Tabaco/Nicotina.
   - Segunda ordem: DMSO, Arnica, Florais, Dipirona, Óleo de Rícino.
   - Candidatas: Azul de Metileno, GLP-1, Metformina, Rapamicina, NAC.
3. Depois converter Tetraciclina e Doxiciclina em fichas HTML usando a ficha da Ivermectina como template.

---

## 10. Fontes PKA usadas nesta esquematização

- `Knowledge Base/Biofísica Farmacológica/Framework-Ordem-Terapeutica.md`
- `Knowledge Base/Biofísica Farmacológica/INDEX.md`
- `Knowledge Base/Biofísica Farmacológica/Biofisica da Ivermectina - Framework Jack Kruse.md`
- `Knowledge Base/Biofísica Farmacológica/Biofisica-Tetraciclina-2026-05-23.md`
- `Knowledge Base/Biofísica Farmacológica/Biofisica-Doxiciclina-2026-05-23.md`
- `Knowledge Base/Biofísica Farmacológica/Biofisica-Tabaco-2026-05-26.md`
- `Knowledge Base/Biofísica Farmacológica/Revisao-Clinica-Tabaco-PeterPicolin-2026-05-26.md`
- `Knowledge Base/Biofísica Farmacológica/Biofisica-DMSO-2026-05-23.md`
- `Knowledge Base/Biofísica Farmacológica/Biofisica-Arnica-Montana-6ch-2026-05-25.md`
- `Knowledge Base/Biofísica Farmacológica/Biofisica-Florais-De-Bach-2026-05-25.md`
- `Knowledge Base/Biofísica Farmacológica/Biofisica-Dipirona-Monohidratado-2026-05-23.md`
- `Knowledge Base/Biofísica Farmacológica/Biofisica-Oleo-de-Ricino-2026-06-02.md`
