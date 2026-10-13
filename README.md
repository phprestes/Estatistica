# SME0123 - Estatística: Projetos de Simulação

Dois projetos práticos da disciplina **SME0123 - Estatística**, que usam simulação computacional para resolver problemas de probabilidade.

<p align="center">
  <img alt="Disciplina" src="https://img.shields.io/badge/SME0123-Estat%C3%ADstica-blue?style=for-the-badge">
  <img alt="Instituição" src="https://img.shields.io/badge/ICMC--USP-Universidade%20de%20S%C3%A3o%20Paulo-orange?style=for-the-badge">
</p>

> **Disciplina:** SME0123 - Estatística <br>
> **Professor:** Eduardo Fontoura Costa <br>
> **Instituição:** ICMC-USP

<p align="center">
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python" />
  <img src="https://img.shields.io/badge/Jupyter-F37626?style=for-the-badge&logo=jupyter&logoColor=white" alt="Jupyter" />
  <img src="https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white" alt="NumPy" />
  <img src="https://img.shields.io/badge/pandas-150458?style=for-the-badge&logo=pandas&logoColor=white" alt="pandas" />
  <img src="https://img.shields.io/badge/SciPy-8CAAE6?style=for-the-badge&logo=scipy&logoColor=white" alt="SciPy" />
  <img src="https://img.shields.io/badge/Plotly-3F4F75?style=for-the-badge&logo=plotly&logoColor=white" alt="Plotly" />
</p>

## Requisitos

- **Python 3**
- **Jupyter** (JupyterLab, Notebook, VS Code ou Google Colab)
- `numpy`, `pandas`, `scipy`, `matplotlib`, `plotly`, `tqdm`, `nbformat`

## Como Executar

```bash
pip install numpy pandas scipy matplotlib plotly tqdm nbformat
jupyter lab
```

Abra os arquivos `.ipynb` no ambiente Jupyter.

## Estrutura do Projeto

- `filaCadeiaMarkov.ipynb`: simulação de filas e Cadeias de Markov.
- `tetraedroEsfera.ipynb`: simulação do tetraedro em uma esfera.

## Funcionalidades Implementadas

### Simulação: Filas e Cadeias de Markov

Fila com capacidade finita ($M/M/r/4$) e número variável de atendentes, com chegadas e atendimentos exponenciais. Compara duas estratégias de alocação de servidores:

- **Estratégia A:** 1 servidor fixo (se houver clientes).
- **Estratégia B:** 1 servidor se $X \leq 2$ e 2 servidores se $X > 2$ ($X$ é o número de clientes).

Principais atividades:

- Simulação de trajetórias $X(t)$ (número de clientes ao longo do tempo).
- Teste de hipótese para verificar se a Estratégia B reduz o número médio de clientes no sistema.
- Simulação do tempo total $T$ de um cliente no sistema.
- Comparação das médias e da eficiência entre as estratégias.

### Simulação: Tetraedro em uma Esfera

> "Ao sortear 4 pontos aleatórios em uma esfera de raio $R$, qual é a probabilidade de o tetraedro formado por eles conter o centro da esfera?"

Principais atividades:

- Geração de pontos uniformemente distribuídos na superfície da esfera.
- Teste de uniformidade com o teste Qui-Quadrado ($\chi^2$).
- Visualização 3D interativa dos pontos e tetraedros com `plotly`.
- Estimativa da probabilidade $\hat{p}_N$ com $N$ de $10^3$ a $10^7$.
- Intervalos de confiança para a probabilidade estimada (valor teórico esperado: 1/8 = 0.125).
