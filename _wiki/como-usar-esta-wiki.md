---
title: Como usar esta wiki
order: 1
---

# Como usar esta wiki

1. Crie um arquivo `.md` na pasta `_wiki/`.
2. No início do arquivo, coloque o *front matter* com pelo menos o título:

```yaml
---
title: Nome que aparece na lista
---
```

3. Escreva o restante em **Markdown** normal.
4. Faça commit e push. O [GitHub Pages](https://pages.github.com/) gera o site com Jekyll; a página aparece em `/wiki/nome-do-arquivo/` (sem a extensão `.md`).

Opcionalmente use `order` no front matter se quiser ordenar no futuro (hoje a lista usa ordem alfabética por título).
