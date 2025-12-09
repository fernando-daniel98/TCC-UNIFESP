# TCC-UNIFESP

**Sistema de Agricultura de Precisão para o Manejo Sustentável de Recursos Hídricos baseado na Fusão de Dados de Sensores IoT e Imagens de Satélite**

Trabalho de Conclusão de Curso apresentado ao Instituto de Ciência e Tecnologia da Universidade Federal de São Paulo (UNIFESP) como requisito parcial para obtenção do título de Bacharel em Engenharia de Computação.

---

## Autor

**Fernando Daniel Marcelino**  
Bacharelado em Engenharia de Computação  
Universidade Federal de São Paulo - UNIFESP  
Instituto de Ciência e Tecnologia  
São José dos Campos, SP

**Orientadora:** Profa. Dra. Fernanda Quelho Rossi

---

## Sobre o Projeto

Este projeto propõe o desenvolvimento de um sistema de agricultura de precisão focado no manejo hídrico sustentável, baseado na fusão de dados provenientes de sensores IoT instalados em campo e de imagens de satélite. O objetivo é gerar mapas de recomendação de irrigação mais precisos e eficientes, contribuindo para:

- **ODS 2**: Fome Zero e Agricultura Sustentável
- **ODS 6**: Água Potável e Saneamento
- **ODS 12**: Consumo e Produção Responsáveis

### Objetivos Específicos

1. Revisar a literatura sobre IoT, sensoriamento remoto e técnicas de fusão de dados aplicadas à agricultura de precisão
2. Definir a arquitetura do sistema de coleta e armazenamento de dados
3. Estabelecer metodologia para aquisição e processamento de imagens de satélite
4. Desenvolver modelo de _machine learning_ para fusão de dados
5. Implementar protótipo do sistema com _dashboard_ de recomendação
6. Analisar a eficácia na redução do desperdício de água

---

## Estrutura do Repositório

```
TCC-UNIFESP/
├── docs/                      # Documentação completa
│   ├── written/              # Monografia em LaTeX
│   └── presentations/        # Apresentações Beamer
│       ├── defesa/          # Apresentação de defesa
│       ├── qualificacao/    # Apresentação de qualificação
│       └── seminarios/      # Outras apresentações
│
├── data/                     # Dados do projeto (não versionados)
│   ├── raw/                 # Dados brutos
│   ├── interim/             # Dados intermediários
│   ├── processed/           # Dados processados
│   └── external/            # Dados externos (shapefiles, etc.)
│
├── models/                   # Modelos treinados (não versionados)
│   ├── checkpoints/         # Checkpoints de treinamento
│   └── final/               # Modelos finais
│
├── notebooks/               # Jupyter notebooks para análise
│
├── results/                 # Resultados e produtos
│   ├── figures/            # Figuras para monografia
│   ├── maps/               # Mapas temáticos
│   ├── reports/            # Relatórios gerados
│   └── metrics/            # Métricas de desempenho
│
├── hardware/                # Documentação de hardware IoT
│   ├── schematics/         # Esquemas elétricos
│   ├── firmware/           # Código para ESP32
│   └── datasheets/         # Datasheets dos componentes
│
├── config/                  # Arquivos de configuração
├── scripts/                 # Scripts auxiliares
├── tests/                   # Testes unitários
│
├── .gitignore
├── requirements.txt         # Dependências Python
└── README.md               # Este arquivo
```

Cada diretório principal contém um `README.md` com documentação detalhada.

---

## Começando

### Pré-requisitos

- **Python**: 3.9 ou superior
- **LaTeX**: TeX Live (Linux), MiKTeX (Windows) ou MacTeX (macOS)
- **Git**: para controle de versão
- **Conda** ou **venv**: para ambiente virtual Python

### Instalação

1. **Clone o repositório:**
   ```bash
   git clone https://github.com/fernando-daniel98/TCC-UNIFESP.git
   cd TCC-UNIFESP
   ```

2. **Crie e ative um ambiente virtual:**
   ```bash
   # Com conda
   conda create -n tcc-unifesp python=3.9
   conda activate tcc-unifesp

   # Ou com venv
   python -m venv venv
   source venv/bin/activate  # Linux/macOS
   .\venv\Scripts\Activate   # Windows
   ```

3. **Instale as dependências Python:**
   ```bash
   pip install -r requirements.txt
   ```

4. **Configure as credenciais (se necessário):**
   ```bash
   cp config/credentials.env.example config/credentials.env
   # Editar credentials.env com suas chaves
   ```

### Compilando a Monografia

```bash
cd docs/written
pdflatex monografia_EC.tex
bibtex monografia_EC
pdflatex monografia_EC.tex
pdflatex monografia_EC.tex
```

Ou com `latexmk`:
```bash
latexmk -pdf monografia_EC.tex
```

---

## Uso

### Executar Análise Exploratória
```bash
jupyter notebook notebooks/01_exploratory_data_analysis.ipynb
```

### Processar Dados de Satélite
```bash
python scripts/download_satellite_data.py \
  --start-date 2025-01-01 \
  --end-date 2025-12-31 \
  --cloud-cover 20
```

### Treinar Modelo
```bash
python scripts/train_model.py \
  --model random_forest \
  --features data/processed/features.csv \
  --target umidade_solo
```

### Gerar Mapa de Irrigação
```bash
python scripts/generate_irrigation_map.py \
  --model models/final/rf_v1.0.pkl \
  --features data/processed/features_20251208.tif \
  --output results/maps/
```

---

## Testes

```bash
pytest tests/
```

---

## Status do Desenvolvimento

- [x] Estruturação do repositório
- [x] Fundamentação teórica
- [ ] Coleta de dados IoT (Caminho B)
- [ ] Processamento de imagens de satélite
- [ ] Fusão de dados
- [ ] Treinamento de modelos
- [ ] Validação
- [ ] Dashboard de recomendação
- [ ] Escrita da monografia
- [ ] Preparação da defesa

---

## Documentação Adicional

- [Documentação Completa](docs/README.md)
- [Estrutura de Dados](data/README.md)
- [Notebooks](notebooks/README.md)
- [Hardware IoT](hardware/README.md)
- [Scripts](scripts/README.md)

---

## Contribuindo

Este é um projeto acadêmico individual. Sugestões e feedback são bem-vindos através de _issues_.

---

## Licença

Este projeto é desenvolvido para fins acadêmicos como parte do Trabalho de Conclusão de Curso.

---

## Contato

**Fernando Daniel Marcelino**  
LinkedIn:  [fernando-daniel](https://www.linkedin.com/in/fernando-daniel/)
GitHub: [@fernando-daniel98](https://github.com/fernando-daniel98)

**Orientadora**  
Profa. Dra. Fernanda Quelho Rossi  
UNIFESP - Instituto de Ciência e Tecnologia

---

## Agradecimentos

- Profa. Dra. Fernanda Quelho Rossi pela orientação
- UNIFESP - Instituto de Ciência e Tecnologia

---

## Citação

Se você utilizar este trabalho, por favor cite:

```bibtex
@mastersthesis{marcelino2025tcc,
  author  = {Fernando Daniel Marcelino},
  title   = {Sistema de Agricultura de Precisão para o Manejo Sustentável 
             de Recursos Hídricos baseado na Fusão de Dados de Sensores 
             IoT e Imagens de Satélite},
  school  = {Universidade Federal de São Paulo},
  year    = {2025},
  address = {São José dos Campos, SP},
  type    = {Trabalho de Conclusão de Curso}
}
```

---

**Última atualização:** Dezembro de 2025
