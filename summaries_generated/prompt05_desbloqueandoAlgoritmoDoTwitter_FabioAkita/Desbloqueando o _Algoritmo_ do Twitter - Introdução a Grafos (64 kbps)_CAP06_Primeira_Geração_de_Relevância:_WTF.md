# Resumo do Capítulo 06 - "Primeira Geração de Relevância: WTF"

Neste capítulo, são abordados conceitos relacionados à primeira geração de relevância no Twitter, com destaque para o uso de grafos, regressão logística e similaridade de cosseno. Além disso, são mencionados os projetos Castlevary e FlockDB, que desempenharam papéis importantes no processamento e armazenamento dos dados.

### WTF - What the fuck? Não, era Rootfollow

No início da implementação de recomendações de usuários no Twitter, por volta de 2010, o sistema utilizado era conhecido como Rootfollow. Esse sistema tinha como base a utilização de grafos bipartidos, com usuários em um lado e tweets no outro. A ideia era recomendar novos usuários para seguir com base no comportamento dos usuários existentes.

### O Projeto Castlevary e o Processamento de Grafos

O projeto Castlevary foi um motor de processamento de grafos em memória utilizado pelo Twitter naquela época. Ele operava com snapshots de grafos de seguidores, que eram carregados do HDFS (Hadoop Distributed File System), um sistema de arquivos distribuído. O Castlevary mantinha os grafos em memória para realizar cálculos e análises. Esse projeto é open source e pode ser encontrado no GitHub, embora não seja mais utilizado atualmente.

### FlockDB - O Banco de Dados de Grafos do Twitter

O FlockDB foi o primeiro banco de dados de grafos desenvolvido pelo Twitter e posteriormente disponibilizado como open source. Ele foi utilizado para armazenar os grafos de seguidores, oferecendo maior desempenho para operações de inserção e atualização em comparação aos bancos de dados relacionais. O FlockDB permitia realizar operações de navegação nos nós e vértices do grafo. A carga de um grafo em memória pode ser pesada, especialmente considerando o grande volume de dados presente no Twitter.

### Limitações e Desafios

Uma das limitações da época era que as sugestões de recomendação de quem seguir eram calculadas em lotes (batch), ou seja, apenas uma vez por dia, ao contrário do tempo real utilizado atualmente. Além disso, o crescimento do volume de dados dos grafos representava um desafio em relação à capacidade de memória dos servidores.

### Círculo de Confiança e Salsa

Durante as experimentações e testes AB realizados, o Twitter chegou a dois conceitos que ainda são utilizados: o "Círculo de Confiança" e a adoção do "Salsa" (Stochastic Approach for Link Structure Analysis - Análise de Estrutura de Links Usando Processos Estocásticos). Detalhes adicionais sobre esses conceitos não são fornecidos no trecho do vídeo.

*Ressalvas sobre informações inconsistentes:*

Neste trecho do vídeo, não foram encontradas informações incorretas. No entanto, alguns conceitos e detalhes mencionados podem exigir pesquisas adicionais para obter informações mais detalhadas sobre o funcionamento e a implementação específica dos mesmos.