# NewProjectsConfigs

Configurações e arquivos-base para iniciar novos projetos com padrões consistentes desde o primeiro commit.

## Objetivo

Evitar repetir configuração básica a cada projeto e manter uma base mínima, previsível e fácil de evoluir.

## Estrutura

```text
.
├── AGENTS.md
├── js-ts/
│   ├── .gitignore
│   └── .prettierrc.json
├── py/
│   ├── .gitignore
│   └── pyproject.toml
└── rust/
    ├── .gitignore
    └── rustfmt.toml
```

### JavaScript / TypeScript

`js-ts/.prettierrc.json` define uma configuração compartilhada do Prettier:

- 2 espaços de indentação
- aspas simples
- ponto e vírgula
- trailing commas
- largura máxima de 80 caracteres
- LF como final de linha

### Python

`py/pyproject.toml` configura o Ruff para Python 3.10, com regras de estilo, imports, modernização de sintaxe, segurança e padrões propensos a bugs.

### Rust

`rust/rustfmt.toml` define regras para organização de imports, largura de linha e estilo de blocos de controle. Também documenta opções que dependem do Rust Nightly.

## AGENTS.md

O `AGENTS.md` define as regras de trabalho do repositório, com foco em:

- commits atômicos;
- mudanças pequenas e isoladas;
- histórico Git limpo e reversível;
- evitar alterações fora do escopo;
- preservar mudanças existentes;
- perguntar quando uma decisão importante não puder ser determinada com segurança;
- reduzir inspeções e alterações desnecessárias para economizar tokens.

## Uso

Copie os arquivos da linguagem desejada para o novo projeto e adapte apenas o que for específico à aplicação.

A ideia é começar com uma base consistente, não transformar configurações compartilhadas em uma religião. Se o projeto tiver uma necessidade real diferente, a configuração deve ser ajustada conscientemente.

## Licença

Este projeto está disponível sob a [MIT License](LICENSE).
