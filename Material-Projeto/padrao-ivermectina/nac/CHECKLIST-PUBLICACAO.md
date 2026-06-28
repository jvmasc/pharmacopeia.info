# CHECKLIST PRÉ-PUBLICAÇÃO — NAC (padrão ivermectina)

## Diretórios e ficheiros
- [ ] Material-Projeto/padrao-ivermectina/nac/ existe
- [ ] DOSSIER.md presente e completo
- [ ] HISTORIA.md presente e completo
- [ ] ROTEIRO-IMAGENS.md presente e completo
- [ ] PROMPTS-IMAGENS.md presente e completo
- [ ] CHECKLIST-PUBLICACAO.md presente e completo
- [ ] assets/moleculas/nac/gpt/ existe
- [ ] assets/moleculas/nac/gpt/nac-01-molecula-gpt.png presente
- [ ] assets/moleculas/nac/gpt/nac-02-mecanismo-gpt.png presente
- [ ] assets/moleculas/nac/gpt/nac-03-mapa-farmacologico-gpt.png presente
- [ ] assets/moleculas/nac/gpt/nac-04-interface-biofisica-gpt.png presente

## moleculas/nac/index.html — Head
- [ ] DOCTYPE html lang="pt-BR"
- [ ] Meta charset utf-8
- [ ] Meta viewport
- [ ] Title: "N-Acetilcisteína (NAC) — Pharmacopeia.info"
- [ ] Meta description educacional
- [ ] Anti-FOWT script (localStorage ph-theme antes de render)
- [ ] Google Fonts: Spectral + Space Mono
- [ ] Style: tokens CSS light/dark
- [ ] --paper: #F7F4EE, --ink: #1A1E1C, --solar: #9A6B18, --bio: #1E6E6A, --mag: #4A3E9C
- [ ] Tokens dark mapeados corretamente

## moleculas/nac/index.html — Header
- [ ] Brand link a ../../index.html
- [ ] Mark circular com .mark-dot
- [ ] Nav: biofisica, bioquimica, evidencia, fontes
- [ ] Theme toggle button (texto "escuro"/"claro")

## moleculas/nac/index.html — Hero
- [ ] Kicker: "Ficha · molécula"
- [ ] h1: "N-Acetilcisteína (NAC)"
- [ ] Lead: "A bula vê..." com strong inicial
- [ ] CTA row com 2 buttons (#biofisica, #bioquimica)

## moleculas/nac/index.html — Painel duplo (tese + guardrail)
- [ ] grid-2 com article.panel + aside.notice.warning
- [ ] Tese pública (1 parágrafo NAC como removedor de obstáculo)
- [ ] Guardrail: educacional, sem prescrição, interações com nitratos, risco anafilático IV

## moleculas/nac/index.html — Summary cards
- [ ] Section head: kicker + h2 + p
- [ ] grid-3 com 6 summary-card
- [ ] Cards: status tags (established, hypothesis, investigational, guarded)
- [ ] 6 cartões com conteúdo NAC

## moleculas/nac/index.html — #figuras
- [ ] Section id="figuras"
- [ ] Section head com kicker + h2 + p
- [ ] figure-grid 2×2
- [ ] 4 figure-card com img + figcaption
- [ ] Paths corretos: ../../assets/moleculas/nac/gpt/nac-0X-*.png
- [ ] loading="lazy" em cada img
- [ ] Alt text descritivo

## moleculas/nac/index.html — #biofisica
- [ ] Section id="biofisica"
- [ ] Section head com kicker "BLOCO 1 — Biofísica"
- [ ] axis-grid 4-col (8 axis-card)
- [ ] Eixos: origem, arquitectura, espectro, água, CISS, redox, campo, janela
- [ ] Cada axis-card: .num, h3, p, small

## moleculas/nac/index.html — #bioquimica
- [ ] Section id="bioquimica"
- [ ] Section head com kicker "BLOCO 2 — Bioquímica"
- [ ] grid-2 com 2 panels (mecanismo clássico + farmacocinética/indicações)
- [ ] Panel extra de riscos/interações

## moleculas/nac/index.html — #janela
- [ ] Section id="janela"
- [ ] Section head com kicker "Janela de uso"
- [ ] grid-2 com pré-requisitos + limites absolutos

## moleculas/nac/index.html — #evidencia
- [ ] Section id="evidencia"
- [ ] Section head com kicker "Estado da evidência"
- [ ] grid-2 com camadas (verde/ciano/âmbar/vermelho) + nota metodológica

## moleculas/nac/index.html — #fontes
- [ ] Section id="fontes"
- [ ] grid-3 com source-card ligando às 3 monografias
- [ ] Ligação correta às monografias existentes

## moleculas/nac/index.html — Guardrail final
- [ ] Notice warning com guardrail clínico completo

## moleculas/nac/index.html — Footer
- [ ] Footer com brand + tag educacional

## moleculas/nac/index.html — Script
- [ ] Theme toggle JS funcional
- [ ] applyTheme(), localStorage, event listener

## moleculas/nac/index.html — Responsivo
- [ ] axis-grid 2-col a 1000px
- [ ] nav hiding a 760px
- [ ] grids single-column a 760px
- [ ] prefers-reduced-motion

## Auditoria
- [ ] Nenhum placeholder "${...}" ou "TODO" no HTML
- [ ] Todos os links internos válidos (#biofisica, #bioquimica, #evidencia, #fontes, #figuras, #janela)
- [ ] ../../index.html link funcional
- [ ] Caminhos das imagens relativos corretos
- [ ] Âncoras HTML balanceadas (abertura/fecho de tags)
- [ ] Validação visual cruzada entre ivermectina e NAC
- [ ] Sem dosagem, ciclo ou posologia
- [ ] Guardrail visível em 2 locais (painel + final)
- [ ] Hipóteses Kruse/PKA marcadas como investigacional
