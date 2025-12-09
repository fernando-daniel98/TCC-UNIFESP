# Apresentação de Defesa - TCC UNIFESP

Esta pasta contém a apresentação de defesa do TCC desenvolvida em LaTeX usando o pacote Beamer.

## Estrutura

```
defesa/
├── defesa.tex          # Arquivo principal da apresentação
├── sections/           # Slides organizados por seção (opcional)
├── figures/            # Figuras e imagens específicas
└── README.md          # Este arquivo
```

## Compilação

### Método 1: pdflatex (Básico)
```bash
cd docs/presentations/defesa
pdflatex defesa.tex
pdflatex defesa.tex  # Compilar duas vezes para referências
```

### Método 2: latexmk (Recomendado)
```bash
latexmk -pdf defesa.tex
```

### Método 3: VS Code com LaTeX Workshop
1. Instalar extensão "LaTeX Workshop"
2. Abrir `defesa.tex`
3. Ctrl+Alt+B (compilar) ou Ctrl+Alt+V (visualizar)

## Personalização

### Temas Disponíveis
O template usa o tema `Madrid` por padrão. Outros temas interessantes:

- **Clássicos**: `Boadilla`, `CambridgeUS`, `Warsaw`
- **Modernos**: `Berlin`, `Copenhagen`, `Malmoe`
- **Minimalistas**: `default`, `boxes`, `Pittsburgh`

Para alterar, modifique a linha:
```latex
\usetheme{Madrid}  % Trocar por outro tema
```

### Esquemas de Cores
O template usa cores personalizadas da UNIFESP. Esquemas alternativos:

- `beaver` (vermelho)
- `crane` (laranja)
- `dolphin` (azul claro)
- `whale` (azul escuro)
- `seahorse` (roxo)

Para alterar:
```latex
\usecolortheme{beaver}  % Trocar esquema
```

### Aspect Ratio
O template usa 16:9 por padrão. Para alterar:

```latex
\documentclass[aspectratio=169]{beamer}  % 16:9 (padrão)
\documentclass[aspectratio=43]{beamer}   % 4:3 (projetores antigos)
\documentclass[aspectratio=1610]{beamer} % 16:10 (notebooks)
```

## Estrutura do Template

### Seções Incluídas

1. **Introdução**
   - Contextualização
   - Motivação
   - Objetivos

2. **Fundamentação Teórica**
   - Internet das Coisas (IoT)
   - Sensoriamento Remoto
   - Fusão de Dados

3. **Metodologia**
   - Área de estudo
   - Pipeline de processamento
   - Arquitetura do sistema

4. **Resultados**
   - Análise exploratória
   - Desempenho dos modelos
   - Mapas de irrigação
   - Dashboard

5. **Discussão**
   - Contribuições
   - Limitações
   - Trabalhos futuros

6. **Conclusão**

7. **Apêndice (Backup Slides)**
   - Referências
   - Detalhes técnicos adicionais

## Adicionando Figuras

### Placeholder
Atualmente, o template usa placeholders para as figuras:
```latex
\includegraphics[width=\textwidth]{figures/nome_figura.png}
```

### Adicionar Figuras Reais
1. Salve as figuras em `figures/`
2. Formate PNG (300 DPI) ou PDF (vetorial)
3. Nomeie de forma descritiva: `iot_architecture.png`, `study_area.pdf`, etc.

### Figuras Necessárias
- [ ] `logo-unifesp.pdf` (logo da UNIFESP)
- [ ] `iot_architecture.png` (diagrama de arquitetura IoT)
- [ ] `sentinel2_rgb.png` (composição RGB Sentinel-2)
- [ ] `study_area.png` (mapa da área de estudo)
- [ ] `sensor_node.png` (foto/esquema do nó sensor)
- [ ] `timeseries_iot.png` (série temporal de sensores)
- [ ] `timeseries_ndvi.png` (série temporal de NDVI)
- [ ] `irrigation_map.png` (mapa de recomendação)
- [ ] `dashboard.png` (screenshot do dashboard)

## Diagramas TikZ

O template inclui um diagrama de fluxo usando TikZ:

```latex
\begin{tikzpicture}[...]
  \node[box] (iot) {Sensores IoT};
  \node[box] (sat) {Satélite};
  % ...
\end{tikzpicture}
```

Vantagens do TikZ:
- Gráficos vetoriais (escalam perfeitamente)
- Integração nativa com LaTeX
- Customização total

## Modo Apresentação

### Notas do Apresentador
Para adicionar notas visíveis apenas no modo apresentador:

```latex
\usepackage{pgfpages}
\setbeameroption{show notes on second screen=right}

\begin{frame}{Título}
  Conteúdo do slide
  \note{Nota para o apresentador: lembrar de mencionar X}
\end{frame}
```

### Transições
Para adicionar transições entre slides:

```latex
\transduration<0->{0.5}  % Duração da transição
\transboxin              % Tipo de transição
```

## Apresentação Efetiva

### Tempo Recomendado
- **Total**: 20-30 minutos (depende da banca)
- **Introdução**: 3-4 min
- **Fundamentação**: 4-5 min
- **Metodologia**: 6-8 min
- **Resultados**: 8-10 min
- **Discussão/Conclusão**: 3-4 min

### Dicas
1. **Máximo 5-6 bullets por slide**
2. **Fontes grandes** (Beamer já usa tamanhos adequados)
3. **Contraste alto** (evitar amarelo claro, azul claro)
4. **Figuras grandes** e de alta qualidade
5. **Praticar a apresentação** múltiplas vezes
6. **Backup slides** para perguntas antecipadas

## Exportação

### PDF Final
```bash
# Gera defesa.pdf na pasta atual
pdflatex defesa.tex
```

### Compressão (Opcional)
Se o PDF ficar muito grande (> 10MB):

```bash
# Linux/macOS
gs -sDEVICE=pdfwrite -dCompatibilityLevel=1.4 -dPDFSETTINGS=/screen \
   -dNOPAUSE -dQUIET -dBATCH -sOutputFile=defesa_compressed.pdf defesa.pdf

# Windows (instalar Ghostscript)
gswin64c -sDEVICE=pdfwrite -dCompatibilityLevel=1.4 -dPDFSETTINGS=/screen ^
         -dNOPAUSE -dQUIET -dBATCH -sOutputFile=defesa_compressed.pdf defesa.pdf
```

## Recursos Adicionais

### Temas Beamer
- [Beamer Theme Matrix](https://hartwork.org/beamer-theme-matrix/)
- [Overleaf Beamer Themes](https://www.overleaf.com/learn/latex/Beamer_Themes)

### Cores
- [LaTeX Color Names](https://www.overleaf.com/learn/latex/Using_colours_in_LaTeX)
- [Beamer Color Themes](https://deic.uab.cat/~iblanes/beamer_gallery/index_by_color.html)

### TikZ
- [TikZ Examples](https://texample.net/tikz/examples/)
- [TikZ and PGF Manual](http://mirrors.ctan.org/graphics/pgf/base/doc/pgfmanual.pdf)

### Templates Adicionais
- [LaTeX Beamer Theme Gallery](https://deic.uab.cat/~iblanes/beamer_gallery/)
- [Overleaf Templates](https://www.overleaf.com/gallery/tagged/presentation)

## Checklist Pré-Defesa

- [ ] Todas as figuras incluídas e com boa qualidade
- [ ] Logo da UNIFESP presente no título
- [ ] Referências completas nos backup slides
- [ ] Numeração de slides habilitada
- [ ] Testar em projetor/tela externa
- [ ] PDF final gerado e testado
- [ ] Apresentação cronometrada (< 30 min)
- [ ] Notas do apresentador preparadas (se usar)
- [ ] Backup do PDF em múltiplos dispositivos
- [ ] Respostas para perguntas previstas preparadas

## Contato

Em caso de dúvidas sobre o template ou LaTeX:

- **Overleaf Community**: https://www.overleaf.com/learn
- **TeX StackExchange**: https://tex.stackexchange.com/
- **Beamer Documentation**: `texdoc beamer` (terminal)

Boa sorte na defesa! 🎓
