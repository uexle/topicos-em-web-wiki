# Wiki em Markdown (GitHub Pages)

Site estático com [Jekyll](https://jekyllrb.com/), pronto para [GitHub Pages](https://docs.github.com/pages). Cada arquivo em `_wiki/` vira uma página; a lista na página inicial é gerada automaticamente.

## Conteúdo

| Caminho | Função |
|--------|--------|
| `_wiki/*.md` | Artigos da wiki (um arquivo = uma página) |
| `index.md` | Página inicial com a lista de artigos (`site.wiki`) |
| `_config.yml` | Tema, collection `wiki`, URLs |

## Publicar no GitHub Pages

1. Crie um repositório no GitHub e envie este projeto (`git init`, commit, `git remote`, `push`).
2. No repositório: **Settings → Pages**.
3. Em **Build and deployment**:
   - **Source**: *GitHub Actions* não é obrigatório para este projeto; use **Deploy from a branch**.
   - **Branch**: `main` (ou `master`) e pasta **`/` (root)**.
4. Salve. Em poucos minutos o site ficará em:
   - **Repositório de usuário** `usuario.github.io`: `https://usuario.github.io/`
   - **Repositório de projeto** `usuario/repo`: `https://usuario.github.io/repo/`

Se o site for de **projeto** (ex.: `https://uexle.github.io/topicos-em-web-wiki/`), **é obrigatório** definir `url` e `baseurl`. Sem `baseurl`, o tema Minima aponta CSS/JS para a raiz do domínio e a página fica sem estilo.

```yaml
url: "https://SEU-USUARIO.github.io"
baseurl: "/NOME-DO-REPO"   # mesmo nome do repositório, com barra inicial, sem barra final
```

Se renomear o repositório, atualize `baseurl` para o novo nome.

## Incluir um artigo novo

1. Adicione `meu-artigo.md` em `_wiki/`.
2. Coloque no topo do arquivo:

```yaml
---
title: Título na lista
---
```

3. Commit e push. O artigo aparece na lista da home e em `/wiki/meu-artigo/`.

## Testar localmente

Requer [Ruby](https://rubyinstaller.org/) e [Bundler](https://bundler.io/).

```bash
cd "3 - Wiki"
bundle install
bundle exec jekyll serve
```

Abra `http://127.0.0.1:4000` (se usar `baseurl`, acesse `http://127.0.0.1:4000/nome-do-repo`).

## Stack

- **Jekyll** + tema **minima** (suportado nativamente pelo GitHub Pages, sem workflow obrigatório).
