# Apresentações do TCC

Este diretório contém todas as apresentações desenvolvidas ao longo do TCC.

## Estrutura

### `defesa/`
Apresentação final de defesa do TCC.

- **Arquivo principal**: `defesa.tex`
- **Duração**: 20-30 minutos
- **Público**: Banca examinadora
- **Status**: Em desenvolvimento

### `qualificacao/`
Apresentação de qualificação (se aplicável ao curso).

- Apresentação intermediária do projeto
- Foco em metodologia e resultados preliminares
- Feedback para ajustes antes da defesa final

### `seminarios/`
Outras apresentações relacionadas ao projeto.

- Apresentações em disciplinas
- Seminários de pesquisa
- Eventos acadêmicos
- Workshops

## Tecnologia

Todas as apresentações são desenvolvidas em **LaTeX** usando o pacote **Beamer**.

### Vantagens do Beamer
- Integração nativa com LaTeX
- Fórmulas matemáticas de alta qualidade
- Consistência de formatação
- Controle fino sobre layout
- Suporte a diagramas TikZ
- Exportação direta para PDF

## Template Padrão

As apresentações seguem um template base com:

- **Tema**: Madrid (customizável)
- **Cores**: UNIFESP (azul e verde)
- **Aspect ratio**: 16:9 (padrão para projetores modernos)
- **Logo**: UNIFESP no slide de título
- **Estrutura**: Introdução → Fundamentação → Metodologia → Resultados → Conclusão

## Compilação

### Compilar todas as apresentações
```bash
# Linux/macOS
cd docs/presentations/defesa && latexmk -pdf defesa.tex
cd docs/presentations/qualificacao && latexmk -pdf qualificacao.tex

# Windows PowerShell
cd docs\presentations\defesa; latexmk -pdf defesa.tex
cd docs\presentations\qualificacao; latexmk -pdf qualificacao.tex
```

### Limpar arquivos auxiliares
```bash
# Linux/macOS
find . -name "*.aux" -o -name "*.log" -o -name "*.nav" -o -name "*.snm" -delete

# Windows PowerShell
Get-ChildItem -Recurse -Include *.aux,*.log,*.nav,*.snm | Remove-Item
```

## Recursos de Figuras

### Localização
- Figuras compartilhadas: `../../results/figures/`
- Figuras específicas da apresentação: `<apresentacao>/figures/`

### Formato Recomendado
- **Vetorial** (preferencial): PDF, SVG
- **Raster** (se necessário): PNG com 300 DPI mínimo
- **Capturas de tela**: PNG com boa resolução

### Otimização
- Simplificar gráficos para apresentação (menos detalhes)
- Usar cores de alto contraste
- Aumentar tamanho de fontes em gráficos
- Testar legibilidade em projetor

## Paleta de Cores UNIFESP

```latex
% Azul UNIFESP
\definecolor{unifespblue}{RGB}{0,51,102}

% Verde UNIFESP
\definecolor{unifespgreen}{RGB}{0,153,102}
```

## Boas Práticas

### Conteúdo
1. **Máximo 1 ideia principal por slide**
2. **Regra 6x6**: máximo 6 bullets, 6 palavras cada
3. **Evitar parágrafos longos**: use bullets e frases curtas
4. **Figuras grandes**: ocupar ≥ 50% do slide quando possível
5. **Contraste**: texto escuro em fundo claro (ou vice-versa)

### Design
1. **Consistência**: usar mesmo tema/cores em toda apresentação
2. **Hierarquia visual**: título > subtítulo > corpo
3. **Espaço em branco**: não poluir os slides
4. **Alinhamento**: elementos bem alinhados
5. **Fontes**: tamanho mínimo 18pt para corpo

### Apresentação
1. **Praticar múltiplas vezes**
2. **Cronometrar rigorosamente**
3. **Preparar respostas para perguntas esperadas**
4. **Testar equipamento antecipadamente**
5. **Ter backup em múltiplos dispositivos**

## Cronograma de Apresentações

| Evento | Data Prevista | Duração | Status |
|--------|---------------|---------|--------|
| Seminário Intermediário | - | 15 min | Não agendado |
| Qualificação | - | 30 min | A definir |
| Defesa Final | Dez 2025 | 30 min | Em preparação |

## Checklist Geral

### Antes da Apresentação
- [ ] Conteúdo revisado pela orientadora
- [ ] Ortografia e gramática verificadas
- [ ] Todas as figuras de alta qualidade
- [ ] Referências completas
- [ ] Apresentação cronometrada
- [ ] PDF testado em computador diferente
- [ ] Backup em nuvem e pen drive

### No Dia da Apresentação
- [ ] Chegar 15 minutos antes
- [ ] Testar projetor e adaptadores
- [ ] Verificar resolução e cores
- [ ] Testar clicker/controle (se usar)
- [ ] Água disponível
- [ ] Celular no silencioso

### Durante a Apresentação
- [ ] Manter contato visual com a banca
- [ ] Falar claramente e em ritmo adequado
- [ ] Usar apontador laser (se necessário)
- [ ] Explicar todas as figuras/gráficos
- [ ] Respeitar o tempo limite

## Ferramentas Úteis

### Apresentação
- **Clicker/Apresentador**: Logitech Spotlight, Kensington
- **Temporizador**: app de celular, relógio
- **Notas**: folhas A4 com tópicos principais

### Prática
- **Gravação**: praticar gravando em vídeo
- **Feedback**: apresentar para colegas
- **Ensaio geral**: simular apresentação completa

## Referências

- [Beamer User Guide](http://mirrors.ctan.org/macros/latex/contrib/beamer/doc/beameruserguide.pdf)
- [The Not So Short Introduction to LaTeX](https://tobi.oetiker.ch/lshort/lshort.pdf)
- [LaTeX Wikibook - Presentations](https://en.wikibooks.org/wiki/LaTeX/Presentations)
- [Overleaf Beamer Documentation](https://www.overleaf.com/learn/latex/Beamer)

## Dicas Finais

> "A apresentação é tão importante quanto o conteúdo. Uma boa pesquisa mal apresentada perde impacto."

- Simplicidade > Complexidade
- Visual > Texto
- Prática > Perfeição teórica
- Confiança vem da preparação

Boa sorte nas apresentações! 🎤📊
