# Wiki — Tópicos Especiais em Desenvolvimento Web

Site estático com [Jekyll](https://jekyllrb.com/) e [GitHub Pages](https://docs.github.com/pages): identidade visual própria (`assets/css/wiki.css` + `_layouts/`), sem depender do tema Minima para o layout.

## Estrutura

| Caminho | Função |
|---------|--------|
| `_wiki/*.md` | Artigos (um arquivo = uma página; aparecem na home como cartões) |
| `index.md` | Texto “Sobre” na home; lista de artigos é gerada pelo layout `home` |
| `_config.yml` | Nome da disciplina (`course`), URLs (`url`, `baseurl`, `repo_url`), collection `wiki` |
| `assets/css/wiki.css` | Cores, tipografia e componentes |
| `_layouts/default.html`, `home.html`, `wiki-article.html` | Estrutura das páginas |

## Personalizar para seu repositório

Em `_config.yml` ajuste:

- `url` e `baseurl` — obrigatório para repositórios de **projeto** (para CSS e links).
- `repo_url` — URL do botão “Repositório” no herói da home.
- `course` — nome completo, sigla, instituição e texto de abertura (`lead`).

## Novo artigo

1. Crie `nome-do-artigo.md` em `_wiki/`.
2. Front matter mínimo:

```yaml
---
title: Título na lista
summary: Opcional — aparece no cartão da home
order: 10
---
```

(`order` opcional; padrão `999`. Valores menores sobem na lista.)

3. *Commit* e *push* → o site publica em `/wiki/nome-do-artigo/`.

Detalhes em [\_wiki/como-usar-esta-wiki.md](_wiki/como-usar-esta-wiki.md).

## GitHub Pages

**Settings → Pages → Deploy from a branch**: branch `main`, pasta `/` (root).

## Testar localmente

```bash
bundle install
bundle exec jekyll serve
```

Com `baseurl` definido, acesse `http://127.0.0.1:4000` + `baseurl` (ex.: `http://127.0.0.1:4000/topicos-em-web-wiki/`).
