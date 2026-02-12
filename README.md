Sistema de Análise e Previsão de Eventos Sísmicos

Sobre o Projeto

Este projeto implementa um pipeline de **Data Science e Estatística** para modelagem de risco sísmico. O sistema analisa dados históricos de terremotos (magnitude 6.5+) e utiliza modelos probabilísticos para prever a ocorrência de futuros eventos em diversas regiões do mundo.

O diferencial deste projeto é a aplicação da **Distribuição de Poisson** para calcular a probabilidade de eventos raros em intervalos de tempo específicos, oferecendo uma ferramenta analítica para estudo de riscos geológicos.

Objetivo
Fornecer uma ferramenta interativa que permita a pesquisadores e entusiastas analisar padrões sísmicos globais e estimar probabilidades de risco com base em dados históricos rigorosos.

## Funcionalidades

*  **Modelagem Probabilística:** Cálculo da probabilidade de ocorrência de $k$ eventos em um período $t$, utilizando distribuição de Poisson baseada na taxa média histórica ($\lambda$).
*  **Análise Comparativa:** Comparação direta de risco sísmico entre dois países ou regiões diferentes.
*  **Consulta Detalhada:** Busca de informações específicas de terremotos históricos via ID único.
*  **Visualização de Dados:** Geração de gráficos de dispersão (Scatter Plots) para análise da profundidade dos abalos ao longo do tempo.
*  **Interface CLI:** Interface de linha de comando robusta e guiada para fácil interação.

## Tecnologias Utilizadas

* **Linguagem:** Python
* **Manipulação de Dados:** Pandas, NumPy
* **Estatística e Matemática:** SciPy (stats)
* **Visualização:** Matplotlib

## Fundamentação Teórica
O sistema baseia-se na premissa de que grandes terremotos podem ser modelados como eventos de Poisson, onde a probabilidade é dada por:

$$P(k \text{ eventos em } t) = \frac{e^{-\lambda t} (\lambda t)^k}{k!}$$

Onde $\lambda$ é a taxa média de ocorrência histórica da região selecionada.

## Estrutura do Projeto
```bash
├── data/               # Base de dados (CSV) de terremotos históricos
├── src/
│   ├── analysis.py     # Lógica de cálculo probabilístico
│   ├── visualization.py # Geração de gráficos
│   └── utils.py        # Funções auxiliares
├── main.py             # Ponto de entrada da aplicação
└── README.md           # Documentação
