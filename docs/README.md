# Documentação de projeto

- Esta pasta contém toda a documentação do projeto.
- Confiram o [tema do projeto](https://docs.google.com/presentation/d/1hRx0g9mpVGQbTv44gLEoAyf4b4kKM4vnrABTnG8HlUk/edit?usp=sharing).
- Confiram o calendário de entregas no [Plano de Ensino](https://docs.google.com/presentation/d/1rfWSq6o3oxLBDlOsa74zmkzughcoZcS-lg7VR7i0qEI/edit?usp=sharing).
- Realizem as entregas através da página da disciplina no Aprender.

## Apresentação final

Confiram as regras de avaliação no [documento do tema do projeto](https://docs.google.com/presentation/d/1hRx0g9mpVGQbTv44gLEoAyf4b4kKM4vnrABTnG8HlUk/edit?usp=sharing).

## MkDocs

A documentação deste repositório é gerada com [MkDocs](https://www.mkdocs.org/) e o tema [Material](https://squidfunk.github.io/mkdocs-material/). Os arquivos Markdown desta pasta (`docs/`) são a fonte do site; a configuração fica em `mkdocs.yml` na raiz do repositório.

### Pré-requisitos

- Python 3 instalado
- `pip` disponível

### Instalação

Na raiz do repositório:

```bash
pip install mkdocs mkdocs-material
```

### Visualizar localmente

Para subir um servidor com recarregamento automático (útil ao editar os `.md`):

```bash
mkdocs serve
```

Abra o endereço indicado no terminal (em geral `http://127.0.0.1:8000`).

### Gerar o site estático

```bash
mkdocs build
```

A saída é gerada na pasta `site/` (não versionar essa pasta).

### Estrutura relevante

```text
mkdocs.yml          # configuração do site (nome, tema, etc.)
docs/
  index.md          # página inicial do site
  *.md              # demais páginas da documentação
  figs/             # figuras e imagens
```

### Dicas

- Edite ou adicione arquivos `.md` em `docs/` e veja o resultado com `mkdocs serve`.
- Ajuste título, tema e navegação em `mkdocs.yml`.
- A publicação no GitHub Pages (branch `gh-pages`) é automatizada por GitHub Actions a cada merge na `main` — não edite `gh-pages` manualmente. Detalhes em [CONTRIBUTING.md](../CONTRIBUTING.md).

Documentação oficial: [mkdocs.org](https://www.mkdocs.org/) · [Material for MkDocs](https://squidfunk.github.io/mkdocs-material/).
