# Resumo do Capítulo 16 - "Introdução a Similarity Clusters: Similaridade de Cosseno"

**Similaridade de Cosseno**

- A similaridade de cosseno é um conceito da álgebra linear usado para medir o quão similar são dois vetores em termos de direção e magnitude.
- É utilizado no contexto do Twitter para calcular a similaridade entre tweets no espaço de SimClusters, que são comunidades de usuários e tweets.
- A similaridade de cosseno varia de 0 a 1, sendo que uma alta pontuação (maior que 0.7) indica que os usuários que gostam de dois tweets compartilham os mesmos SimClusters.

**Vetores e Espaço Vetorial**

- No exemplo dado, foram utilizadas palavras como "Apple" e "banana" para representar documentos indexados.
- Os documentos são representados por vetores em um espaço vetorial, onde cada dimensão corresponde a uma palavra única.
- O vetor de um documento contém a contagem de ocorrências de cada palavra nesse documento.
- Uma consulta de pesquisa também é representada como um vetor, onde as palavras presentes na consulta têm o valor 1 e as ausentes têm o valor 0.
- A similaridade de cosseno entre o vetor de pesquisa e os vetores de documentos é calculada usando o produto escalar entre eles.

**Espaço Vetorial em Escala Maior**

- No exemplo anterior, foram usadas apenas duas palavras, resultando em um espaço vetorial bidimensional.
- No contexto real, o espaço vetorial pode ter centenas de milhares de dimensões, correspondendo ao vocabulário da língua utilizada.
- O conceito de espaço vetorial e a similaridade de cosseno são fundamentais em algoritmos de relevância e recomendação, como o utilizado pelo Twitter.

**SimCluster e Embedding Spaces**

- O projeto Sim Cluster do Twitter utiliza espaços de embedding para calcular a similaridade entre usuários e tweets.
- Embedding Spaces geram representações numéricas dos interesses dos usuários e conteúdos dos tweets.
- No caso do Sim Cluster, ele descobre comunidades de usuários e tweets usando um algoritmo de factorização de matrizes personalizado.
- Essas comunidades são atualizadas a cada três semanas e podem ter milhares até milhões de usuários.