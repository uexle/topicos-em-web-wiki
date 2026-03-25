---
title: Como usar esta wiki
summary: Passo a passo para criar artigos em Markdown na pasta _wiki e publicar no GitHub Pages.
order: 1
---

## Incluir um artigo novo

1. Na raiz do repositório, abra a pasta `_wiki/`.
2. Crie um arquivo `.md` (ex.: `aula-01-http.md`).
3. No topo do arquivo, use o *front matter*:

```yaml
---
title: Título exibido na lista e no topo da página
summary: Uma linha opcional que aparece como resumo no cartão da home.
order: 10
---
```

- **`title`** — obrigatório.
- **`summary`** — opcional; melhora a prévia na grade de artigos.
- **`order`** — opcional; números **menores** aparecem primeiro na home (padrão: `999` se você omitir).

4. Escreva o conteúdo em **Markdown** (títulos, listas, código, links).
5. Faça *commit* e *push*. O GitHub Pages roda o Jekyll e o artigo aparece na home e em `/wiki/nome-do-arquivo/`.

## Boas práticas

- Nomes de arquivo em minúsculas e com hífens (`notas-css-grid.md`).
- Um tópico principal por artigo; quebre textos longos em vários arquivos.
- Imagens: coloque em `assets/images/` e referencie com caminho absoluto do site, por exemplo `![Legenda]({{ site.baseurl }}/assets/images/arquivo.png)` ou use URL relativa ao domínio público após o deploy.

## Referência rápida

| Item | Onde |
|------|------|
| Artigos | `_wiki/*.md` |
| Estilo global | `assets/css/wiki.css` |
| Texto da hero e da disciplina | `_config.yml` → `course` |
| Link do botão “Repositório” | `_config.yml` → `repo_url` |
