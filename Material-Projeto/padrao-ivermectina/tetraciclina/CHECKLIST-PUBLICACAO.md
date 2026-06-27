# Checklist de Publicação — Tetraciclina

> Molécula: **tetraciclina** | Ficha: `moleculas/tetraciclina/index.html`

## Pré-publicação

- [ ] A frase-mãe "A bula vê... A Pharmacopeia lê..." está visível no hero
- [ ] "Esta página é educacional" aparece claramente no guardrail clínico
- [ ] Kicker correto: "Ficha 02 · molécula"
- [ ] Seção `#figuras` com grid de 4 imagens existe
- [ ] Imagens existem nos paths relativos corretos
- [ ] Todas as 4 imagens têm alt text descritivo
- [ ] Alt text não contém "imagem de" — descreve o conteúdo diretamente
- [ ] Seção `#eixos` com 8 cards no grid 4-col
- [ ] Cada eixo tem título, texto e badge de estado epistemológico
- [ ] Seção `#evidencia` com verde/ciano/âmbar/vermelho
- [ ] Seção `#fontes` com fontes internas e externas
- [ ] Regra editorial no final da página
- [ ] Nav inclui link para `#figuras`
- [ ] Links relativos ao homepage (`../../index.html`) funcionam
- [ ] Âncoras internas (`#resumo`, `#figuras`, `#eixos`, `#evidencia`, `#fontes`) existem no HTML

## Conteúdo

- [ ] Sem dose, ciclo, posologia ou recomendação individual
- [ ] Sem promessa de cura, prevenção ou tratamento
- [ ] Hipóteses Kruse/PKA marcadas como hipótese/fronteira investigacional
- [ ] Mecanismo clássico (30S) separado da leitura biofísica
- [ ] História da molécula não usada como prova terapêutica
- [ ] Guardrail específico para tetraciclina: fotossensibilidade, quelação, gravidez/crianças
- [ ] Nenhum "TODO:", "PLACEHOLDER", "lorem ipsum", "inserir aqui", "PENDENTE" no HTML
- [ ] Nenhuma afirmação de CISS, spin, EZ, deutério ou POMC apresentada como consenso
- [ ] Fontes externas citadas existem e são verificáveis

## Imagens

- [ ] Imagem 01 (molécula): fundo claro, traço limpo, sem anúncio
- [ ] Imagem 02 (mecanismo): ribossoma 30S, bloqueio de tRNA
- [ ] Imagem 03 (mapa): ADME com 4-6 nós, legenda de prudência
- [ ] Imagem 04 (interface): hipótese marcada, sem aparência de fato
- [ ] Nenhuma imagem tem aparência de propaganda
- [ ] Nomes de ficheiro seguem o padrão: `<slug>-01-molecula-gpt.png`, `<slug>-02-ribossomo-30s-gpt.png`, `<slug>-03-mapa-farmacologico-gpt.png`, `<slug>-04-interface-biofisica-gpt.png`

## Técnico

- [ ] Página abre localmente sem erros de consola
- [ ] `<!doctype html>` presente
- [ ] `<html lang="pt-BR">`
- [ ] `<meta name="description">` com intenção educacional
- [ ] CSS com variáveis de tema light/dark
- [ ] JS de toggle de tema funcional
- [ ] `loading="lazy"` nas imagens
- [ ] `scroll-margin-top` nas âncoras

## Só depois disto: publicar

- [ ] Git status: apenas ficheiros da tetraciclina alterados
- [ ] Commit: `feat: upgrade tetraciclina ficha to ivermectina standard`
- [ ] Github Pages: esperar 1-5 min após push
- [ ] Verificar URL live: `https://pharmacopeia.info/moleculas/tetraciclina/` → 200
- [ ] Verificar imagens live
