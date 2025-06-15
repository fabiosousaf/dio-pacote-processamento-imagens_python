
# 📦 Descomplicando a Criação de Pacotes em Python

Este repositório contém os materiais e exemplos práticos da apresentação **“Descomplicando a Criação de Pacotes em Python”**, com o objetivo de tornar acessível e direto o processo de empacotar, versionar, documentar e distribuir projetos Python.

## 🎯 Objetivo

Facilitar o entendimento e a criação de pacotes Python reutilizáveis e distribuíveis via PyPI, GitHub ou repositórios internos. O conteúdo é voltado tanto para iniciantes quanto para quem já desenvolve scripts e quer organizar melhor seu código.

---

## 📁 Estrutura de um Pacote Python

A estrutura recomendada é:

```
seu_pacote/
│
├── src/
│   └── seu_pacote/
│       └── __init__.py
│       └── modulo_exemplo.py
│
├── tests/
│   └── test_modulo_exemplo.py
│
├── pyproject.toml
├── README.md
├── LICENSE
└── .gitignore
```

---

## ⚙️ Ferramentas e Boas Práticas

- **Gerenciamento com `pyproject.toml`**  
  Centraliza metadados e dependências (PEP 621).
- **Setuptools como build backend**  
  Configurado no `pyproject.toml` com suporte a versões modernas.
- **Testes automatizados com `pytest`**
- **Linters (`flake8`, `black`) e type checking (`mypy`)**
- **Publicação no PyPI via `twine`**
- **Uso do Git e GitHub para versionamento e distribuição**

---

## 🧪 Exemplo de `pyproject.toml`

```toml
[project]
name = "meu_pacote"
version = "0.1.0"
description = "Exemplo simples de pacote Python"
authors = [{ name = "Seu Nome", email = "email@exemplo.com" }]
dependencies = []

[build-system]
requires = ["setuptools>=61.0"]
build-backend = "setuptools.build_meta"
```

---

## 🚀 Publicação no PyPI

1. Crie uma conta no [PyPI](https://pypi.org)  
2. Gere os arquivos de distribuição:

```bash
python -m build
```

3. Envie com:

```bash
twine upload dist/*
```

---

## 📚 Referências

- [PEP 621 – Storing project metadata in pyproject.toml](https://peps.python.org/pep-0621/)
- [Documentação oficial do setuptools](https://setuptools.pypa.io)
- [Guia oficial do PyPI](https://packaging.python.org/)

---

## 📝 Licença

Este projeto está licenciado sob a [MIT License](LICENSE).
