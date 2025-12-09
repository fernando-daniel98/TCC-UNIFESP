# Apresentação de Seminário - Dezembro 2025

Apresentação do estado atual do projeto TCC para seminário de pesquisa.

## Informações

- **Evento:** Seminário de Pesquisa - Dezembro 2025
- **Data:** 8 de Dezembro de 2025
- **Duração:** 15-20 minutos
- **Arquivo:** `seminario_dezembro_2025.tex`

## Estrutura da Apresentação

1. **Título** - Informações do projeto e autores
2. **Sumário** - Visão geral
3. **Introdução** - Contextualização e motivação
4. **Definição do Problema e Objetivos** - Problema, solução proposta e objetivos
5. **Métodos** - Metodologia e arquitetura do sistema
6. **Resultados** - Status atual e resultados esperados
7. **Conclusões e Trabalhos Futuros** - Próximos passos
8. **Agradecimento** - Contato

## Compilação

```bash
cd docs/presentations/seminarios
pdflatex seminario_dezembro_2025.tex
pdflatex seminario_dezembro_2025.tex
```

Ou com latexmk:
```bash
latexmk -pdf seminario_dezembro_2025.tex
```

## Figuras Necessárias

Criar as seguintes figuras na pasta `docs/presentations/seminarios/figures/`:

- `logo-unifesp.pdf` - Logo da UNIFESP
- `example_irrigation_map.png` - Exemplo conceitual de mapa de irrigação

As outras figuras (se necessário) podem ser referenciadas de `results/figures/`.

## Personalização

Para ajustar cores, tema ou layout, editar as linhas iniciais do arquivo `.tex`:

```latex
\usetheme{Madrid}  % Trocar tema
\usecolortheme{default}  % Trocar esquema de cores
```

Temas alternativos: `Boadilla`, `CambridgeUS`, `Warsaw`, `Berlin`, `Copenhagen`
