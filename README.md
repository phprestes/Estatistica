# SME0123 - Estatística: Projetos de Simulação

Este repositório contém dois projetos práticos desenvolvidos para a disciplina de **SME0123 - Estatística**, ministrada pelo Prof. Eduardo Fontoura Costa no ICMC-USP. Os projetos utilizam métodos de simulação computacional para resolver problemas de probabilidade.

---

## 📂 Conteúdo do Repositório

### 1. Simulação: Filas e Cadeias de Markov (`filaCadeiaMarkov.ipynb`)

Este notebook simula o comportamento de uma fila com capacidade finita ($M/M/r/4$) e número variável de atendentes, analisando o sistema sob a ótica de Processos Estocásticos.

**Cenário:**
* Uma fila onde a taxa de chegada e atendimento seguem distribuições exponenciais.
* Comparação entre duas estratégias de alocação de servidores:
    * **Estratégia A:** 1 servidor fixo (se houver clientes).
    * **Estratégia B:** 1 servidor se $X \leq 2$, e 2 servidores se $X > 2$ (onde $X$ é o número de clientes).

**Principais Atividades:**
* Simulação de trajetórias $X(t)$ (evolução do número de clientes no tempo).
* Teste de Hipótese para verificar se a Estratégia B reduz significativamente o número médio de clientes no sistema.
* Simulação do Tempo Total ($T$) que um cliente passa no sistema.
* Comparação das médias e análise de eficiência entre as estratégias.

### 2. Simulação: Tetraedro em uma Esfera (`tetraedroEsfera.ipynb`)

Este notebook aborda um problema clássico de probabilidade geométrica:
> "Ao sortear 4 pontos aleatórios em uma esfera de raio $R$, qual é a probabilidade de o tetraedro formado por eles conter o centro da esfera?"

**Principais Atividades:**
* Geração de pontos aleatórios uniformemente distribuídos na superfície de uma esfera.
* Teste de uniformidade utilizando o teste Qui-Quadrado ($\chi^2$).
* Visualização 3D interativa dos pontos e tetraedros usando `plotly`.
* Estimativa da probabilidade $\hat{p}_N$ com diferentes tamanhos de amostra ($N$ variando de $10^3$ a $10^7$).
* Cálculo de intervalos de confiança para a probabilidade estimada (o valor teórico esperado é 1/8 ou 0.125).

---

## 🛠️ Tecnologias e Bibliotecas Utilizadas

Os projetos foram desenvolvidos em **Python** utilizando Jupyter Notebooks. As principais bibliotecas necessárias para execução são:

* `numpy`: Para operações vetoriais e geração de números aleatórios.
* `pandas`: Para organização dos resultados em tabelas.
* `scipy`: Para testes estatísticos (Qui-quadrado, Teste-T) e intervalos de confiança.
* `matplotlib`: Para plotagem de gráficos estáticos e histogramas.
* `plotly`: Para visualizações 3D interativas.
* `tqdm`: Para barras de progresso durante as simulações longas.

## 🚀 Como Executar

1. Certifique-se de ter o Python instalado.
2. Instale as dependências:
   ```bash
   pip install numpy pandas scipy matplotlib plotly tqdm nbformat
3. Abra os arquivos .ipynb em um ambiente Jupyter (Jupyter Lab, Notebook, VS Code ou Google Colab).
