# Clusterização com K-Means

Este projeto demonstra a aplicação do algoritmo de clusterização K-Means em um dataset sintético. O objetivo é criar clusters e avaliá-los utilizando diferentes métricas, como o índice de silhueta. Abaixo está uma descrição detalhada do código e dos passos envolvidos.

## Importação das Bibliotecas

As seguintes bibliotecas foram utilizadas:

- **NumPy** e **Pandas**: Para manipulação de dados.
- **Matplotlib**: Para visualização dos dados e resultados.
- **KMeans** do **sklearn**: Para aplicar o algoritmo de clusterização.
- **StandardScaler**: Para padronização dos dados, já que o K-Means é sensível à escala das características.
- **silhouette_score**: Para avaliar a qualidade dos clusters formados.

## Criação do Dataset

- Utilizamos a função `make_blobs` para gerar um dataset sintético com 300 amostras distribuídas em 4 clusters distintos.
- O dataset gerado é utilizado para treinar e testar o algoritmo K-Means.

## Exploração dos Dados

- **`head()`**: Mostra as primeiras linhas do dataset para uma visualização inicial.
- **`describe()`**: Fornece um resumo estatístico das características do dataset, incluindo média, desvio padrão, valores mínimos e máximos.

## Pré-processamento dos Dados

- Como o algoritmo K-Means é sensível à escala dos dados, utilizamos o `StandardScaler` para padronizar as características. Isso garante que todas as características tenham uma média de 0 e desvio padrão de 1.

## Aplicação do Algoritmo K-Means

- O número ideal de clusters é determinado utilizando o **método do cotovelo**. A soma dos quadrados dentro dos clusters (WCSS) é calculada para diferentes números de clusters e é plotado um gráfico para identificar o "cotovelo", que indica o número ideal de clusters.

## Avaliação dos Clusters

- O **índice de silhueta** é calculado para avaliar a qualidade dos clusters. Este índice mede a coesão e separação dos clusters, onde valores próximos de 1 indicam que os clusters estão bem definidos.

## Visualização dos Clusters

- Os clusters formados pelo K-Means são visualizados em um gráfico 2D. Os centróides dos clusters são destacados em vermelho, permitindo uma análise visual da distribuição das amostras e da eficácia do algoritmo.
