# Instrukcja

## Pre Commit

- Dodany został pre-commit mający na celu wyłapanie, czy kod jest poprawnie sformatowany i zgodny z linterem.
- Instrukcja instalacji dostępna na: https://pre-commit.com

## Lokalna instancja

- docker-compose up --build

## Dodawanie nowych paczek do projektu

Do zarządzania zależnościami Python'owymi używamy peotry <https://python-poetry.org/docs/>.

Jeżeli chcemy dodać nową zależność do projektu wpisujemy w konsoli

```
poetry add django="^3.1"
```

W przypadku paczek stricte dev, takich jak, np. flake8 wpisujemy

```
peotry add -dev flake8
```

Następnie tworzymy nowy plik requirements.txt:

```
poetry export --dev --without-hashes -f requirements/base.txt
```

## Formatter

W projekcie głównym formatterem będzie black <https://black.readthedocs.io/en/stable/the_black_code_style.html>. Integruje się on z większością znanych IDE <https://black.readthedocs.io/en/stable/editor_integration.html>.
