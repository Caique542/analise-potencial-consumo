# 🎯 Análise de Expansão de Varejo Esportivo (Market Segmentation)

![Status](https://img.shields.io/badge/Status-Concluído-brightgreen)
![Python](https://img.shields.io/badge/Python-3.10+-blue)
![Lib](https://img.shields.io/badge/Scikit--Learn-Clustering-orange)

## 📄 Descrição do Projeto
Este projeto de **Data Science & Location Intelligence** teve como objetivo mapear o território brasileiro para identificar as cidades com maior potencial para expansão de uma rede de varejo esportivo.

Utilizando dados demográficos e socioeconômicos, foi desenvolvido um **Índice de Potencial de Consumo (IPC)** personalizado e aplicado um algoritmo de **Machine Learning (K-Means)** para segmentar as regiões em clusters estratégicos, permitindo recomendações de investimento baseadas em dados.

## 💼 Problema de Negócio
O desafio consistia em analisar mais de 150 regiões para responder:
* Onde abrir novas lojas físicas?
* Qual o perfil de consumidor de cada região?
* Como priorizar os investimentos de marketing e expansão?

## ⚙️ Metodologia

### 1. Engenharia de Atributos: Criação do IPC
Para rankear as cidades, foi criado o **IPC (Índice de Potencial de Consumo)**. As variáveis foram normalizadas (Z-Score), tratadas contra outliers (Winsorization) e ponderadas conforme relevância para o negócio esportivo:

| Indicador | Peso Atribuído | Justificativa |
| :--- | :---: | :--- |
| **Renda Média per Capita** | 30% | Poder de compra essencial. |
| **População Jovem (10-34 anos)** | 30% | Público-alvo primário do setor esportivo. |
| **Prática de Ativ. Física** | 20% | Demanda latente por produtos. |
| **Escolaridade** | 10% | Correlação com consciência de saúde/bem-estar. |
| **Urbanização** | 10% | Facilidade logística e acesso. |

$$IPC = (Z_{Renda} \cdot 0.3) + (Z_{Jovem} \cdot 0.3) + (Z_{Ativ} \cdot 0.2) + (Z_{Escola} \cdot 0.1) + (Z_{Urban} \cdot 0.1)$$

### 2. Clusterização (Machine Learning)
Utilizei o algoritmo **K-Means** para agrupar as cidades com "DNAs" semelhantes.
* **Definição do K:** O Método do Cotovelo (Elbow Method) indicou que **7 clusters** ofereciam a melhor separação dos dados.


## 📊 Resultados e Personas Encontradas
A segmentação revelou perfis de mercado distintos, guiando a estratégia:

* 🥇 **Mercado de Ouro (Ex: SP, RJ):** Alta renda, público jovem e ativo. **Ação:** Prioridade máxima para lojas conceito.
* 👔 **Mercado Premium Adulto (Ex: DF):** Público maduro, alta escolaridade e renda. **Ação:** Marketing focado em performance e tecnologia.
* ❤️ **Paixão Popular (Ex: Amapá, RN):** Alto engajamento, menor renda. **Ação:** Produtos com bom custo-benefício.
* 📉 **Mercado Maduro Inativo:** Alta renda, mas público idoso e sedentário. **Ação:** Baixa prioridade de expansão.


## 🛠️ Tecnologias Utilizadas
* **Linguagem:** Python
* **Manipulação de Dados:** Pandas, NumPy
* **Machine Learning:** Scikit-learn (K-Means, Preprocessing)
* **Visualização:** Matplotlib, Seaborn

## 🚀 Como Executar
1. Clone o repositório.
2. Instale as dependências: `pip install -r requirements.txt`
3. Execute o notebook `analise_expansao.ipynb`.

---
