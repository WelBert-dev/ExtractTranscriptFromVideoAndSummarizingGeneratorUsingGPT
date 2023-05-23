# Resumo do Capítulo 09 - "Escalando com Hadoop e MapReduce: HDFS e Pig"

## Uso de Hadoop e Apache Pig para Lidar com Big Data
Para melhorar as recomendações, o Twitter decidiu utilizar mais sinais dos logs de comportamento dos usuários, como likes, retweets, replies e follows. No entanto, isso aumentou significativamente os metadados do grafo, tornando inviável manter tudo em memória na primeira versão do motor de recomendação. Para lidar com essa demanda de Big Data, o Twitter optou por utilizar o Hadoop, em particular o Apache Pig, que é um compilador que gera sequências de programas MapReduce.

## Hadoop e HDFS (Hadoop Distributed File System)
O Hadoop é uma plataforma de tecnologias desenvolvida para lidar com o problema de Big Data. O HDFS (Hadoop Distributed File System) é um sistema de arquivos distribuído que faz parte do Hadoop. Ele permite a divisão e armazenamento de dados em vários servidores, permitindo escalabilidade e processamento paralelo de grandes volumes de dados.

## MapReduce
O conceito de MapReduce é fundamental para o processamento de dados em ambientes distribuídos, como o Hadoop. No contexto do processamento de dados em paralelo, o MapReduce envolve a execução de um algoritmo em pedaços dos dados, mapeando os resultados parciais e, em seguida, reduzindo esses resultados para obter a resposta final. É uma abordagem eficiente para o processamento de grandes volumes de dados, dividindo o trabalho em tarefas menores que podem ser executadas em paralelo.

## Problemas com Grafos em MapReduce
Em 2012, quando o Twitter estava desenvolvendo a segunda versão do motor de recomendação, eles encontraram dificuldades em lidar com grafos no ambiente de MapReduce. A maioria dos algoritmos conhecidos para processamento de grafos são iterativos, o que não se encaixa bem na abordagem MapReduce. Essa incompatibilidade tornava o processamento de grafos menos eficiente em ambientes distribuídos como o Hadoop.