# mkdocs-sample

## Prerequisite

[python-poetry](https://python-poetry.org/)

## Installation

```bash
$ poetry install
```

## Spawns a shell within the virtual environment

```bash
$ poetry shell
```

## Preview

```bash
(mkdocs-sample-py3.12) $ mkdocs serve
```

## Creation steps

### Creating a new project folder

```bash
$ mkdir my-project
$ cd my-project
```

### Initialising the poetry

```bash
$ poetry init
```

### Specifying dependencies

```bash
$ poetry add mkdocs-material
$ poetry add mkdocs-with-pdf
$ poetry add plantuml-markdown
```

### Creating new site

```bash
$ poetry shell
(mkdocs-sample-py3.12) $ mkdocs new .
```

### Configuration

mkdocs.yml

```yml
theme:
  name: material
plugins:
  - with-pdf:
      cover: true
      cover_title: My Docs
markdown_extensions:
  - plantuml_markdown:
      server: !ENV [PLANTUML_URL, 'http://localhost:5555']
      format: svg
```
