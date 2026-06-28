# CHECKLIST DE PUBLICAÇÃO — Arnica Montana 6CH

## Pré-publicação

### Conteúdo editorial
- [x] DOSSIER.md criado com classificação, slug, tese, guardrail
- [x] HISTORIA.md com origem, química, história, frase-mãe
- [x] ROTEIRO-IMAGENS.md com 4 imagens descritas
- [x] PROMPTS-IMAGENS.md com prompts GPT-Image-2-Medium + alt text + legendas
- [x] CHECKLIST-PUBLICACAO.md (este ficheiro)

### Imagens
- [ ] 01 — arnica-montana-01-molecula-gpt.png gerada e salva
- [ ] 02 — arnica-montana-02-mecanismo-gpt.png gerada e salva
- [ ] 03 — arnica-montana-03-mapa-farmacologico-gpt.png gerada e salva
- [ ] 04 — arnica-montana-04-interface-biofisica-gpt.png gerada e salva
- [ ] Imagens em assets/moleculas/arnica-montana/gpt/
- [ ] Alt text em todas as <img>
- [ ] Loading="lazy" em todas as <img>

### HTML
- [ ] Anti-FOWT script no <head>
- [ ] Google Fonts: Spectral + Space Mono
- [ ] Tokens CSS: --paper #F7F4EE, --ink #1A1E1C, --solar #9A6B18, --bio #1E6E6A, --mag #4A3E9C
- [ ] Header: brand link a ../../index.html
- [ ] Nav: biofisica, bioquimica, evidencia, fontes
- [ ] Theme toggle button funcional
- [ ] Hero: kicker "Ficha · molécula"
- [ ] Hero: h1 "Arnica Montana 6CH"
- [ ] Hero: lead com frase-mãe
- [ ] Hero: buttons CTA
- [ ] Painel duplo: tese pública + guardrail clínico (warning)
- [ ] Summary cards (grid-3): 6 cards com status tags
- [ ] #figuras: figure-grid 2×2 com 4 imagens e legendas
- [ ] #biofisica: axis-grid 4-col com 8 eixos
- [ ] #bioquimica: farmacologia clássica (2 panels grid-2 + riscos)
- [ ] #janela: terreno, sequência, limites
- [ ] #evidencia: camadas verde/ciano/âmbar/vermelho
- [ ] #fontes: grid-3 source cards
- [ ] Guardrail final (notice warning)
- [ ] Footer com brand e código
- [ ] Theme toggle JS funcional

### Qualidade
- [ ] Sem placeholders (TODO, PLACEHOLDER, lorem, inserir)
- [ ] Todos os links internos funcionais (âncoras #id)
- [ ] Paths das imagens corretos (../../assets/...)
- [ ] Tags HTML balanceadas
- [ ] HTML válido (DOCTYPE, charset, lang)
- [ ] Meta description preenchida
- [ ] Viewport configurado
- [ ] Responsivo (grid collapse em <=760px)
- [ ] Modo escuro funcional
- [ ] prefers-reduced-motion

### Segurança editorial
- [ ] Guardrail "não é prescrição" visível
- [ ] Nenhuma dose, ciclo ou posologia
- [ ] Hipóteses Kruse/PKA marcadas como investigacionais
- [ ] 6CH = caso-fronteira: planta é consenso, diluição é hipótese
- [ ] Planta concentrada (tópica) ≠ diluição 6CH
- [ ] NÃO commitar nem fazer push
