# Resumo do Capítulo 07 - "Relevância nos Primórdios da Web: PageRank e HITS"

## Grafo da World Wide Web
- O grafo da World Wide Web consiste em páginas da internet como nós e os links entre essas páginas como arestas.
- Cada página na internet é representada por um nó, e os links entre as páginas são as arestas.
- No início da web, havia um grande número de páginas, dificultando a busca por informações.
- Antes do surgimento do Google, serviços como Yahoo, Excite, Laicos e outros desempenhavam o papel de diretórios, onde as pessoas poderiam incluir seus sites para serem encontrados.
- O Google introduziu o algoritmo PageRank para melhorar a relevância das páginas na web.

## Algoritmo PageRank
- O PageRank foi desenvolvido pelos fundadores do Google, Larry Page e Sergey Brin, em 1996.
- O PageRank utiliza o conceito de hiperlinks para determinar a relevância de uma página.
- Quanto mais páginas diferentes tiverem links apontando para uma determinada página, mais relevante ela é considerada.
- O algoritmo simula um navegador aleatório que navega pelas páginas e seus links de forma aleatória.
- A probabilidade de o navegador aleatório chegar a uma determinada página é usada como sua pontuação no ranking.
- O PageRank substituiu os diretórios de páginas amarelas, permitindo que um programa vasculhasse as páginas da web, avaliando os links entre elas e atribuindo pontuações de relevância.
- O Google continuou aprimorando o algoritmo PageRank ao longo dos anos e introduziu outras técnicas para combater o spam e melhorar a relevância das pesquisas.

## Web Farms e Trust Rank
- Com o PageRank, surgiram práticas de criação de sites fantasmas (web farms) e manipulação de links para aumentar artificialmente a relevância de uma página.
- O Google evoluiu e começou a usar o Trust Rank, um algoritmo que identifica sites legítimos e desconta a pontuação de sites suspeitos.
- O Google continuou a atualizar seus algoritmos ao longo do tempo para melhorar a qualidade e a relevância dos resultados de pesquisa.

## Limitações do PageRank e Algoritmo HITS
- O PageRank tinha uma limitação de que uma página poderia ser considerada relevante globalmente, mesmo que não fosse relevante para um determinado tópico específico.
- Surgiu o algoritmo HITS (Hyperlink-Induced Topic Search) em 1999, proposto por Jon Kleinberg, para superar essa limitação.
- O HITS atribui duas pontuações distintas a cada página: uma como "hub" (nó central que aponta para várias outras páginas) e outra como "autoridade" (página que recebe links de vários hubs).
- Hubs são páginas que contêm muitos links para outras páginas, enquanto autoridades são páginas que recebem muitos links de hubs.
- O HITS considera a relevância em um domínio específico ou tópico, em vez de uma pontuação global.
- O HITS torna o processo de classificação mais justo, evitando que influenciadores com muitos seguidores sejam automaticamente considerados autoridades.

## Error no generated e returns:

Desculpe pelo corte abrupto anterior. Parece que o texto não foi completamente finalizado. Aqui está o resumo completo dos tópicos abordados no vídeo:


### Grafo da World Wide Web
- O grafo da World Wide Web consiste em páginas da internet como nós e os links entre essas páginas como arestas.
- Cada página na internet é representada por um nó, e os links entre as páginas são as arestas.
- No início da web, havia um grande número de páginas, dificultando a busca por informações.
- Antes do surgimento do Google, serviços como Yahoo, Excite, Laicos e outros desempenhavam o papel de diretórios, onde as pessoas poderiam incluir seus sites para serem encontrados.
- O Google introduziu o algoritmo PageRank para melhorar a relevância das páginas na web.

### Algoritmo PageRank
- O PageRank foi desenvolvido pelos fundadores do Google, Larry Page e Sergey Brin, em 1996.
- O PageRank utiliza o conceito de hiperlinks para determinar a relevância de uma página.
- Quanto mais páginas diferentes tiverem links apontando para uma determinada página, mais relevante ela é considerada.
- O algoritmo simula um navegador aleatório que navega pelas páginas e seus links de forma aleatória.
- A probabilidade de o navegador aleatório chegar a uma determinada página é usada como sua pontuação no ranking.
- O PageRank substituiu os diretórios de páginas amarelas, permitindo que um programa vasculhasse as páginas da web, avaliando os links entre elas e atribuindo pontuações de relevância.
- O Google continuou aprimorando o algoritmo PageRank ao longo dos anos e introduziu outras técnicas para combater o spam e melhorar a relevância das pesquisas.

### Web Farms e Trust Rank
- Com o PageRank, surgiram práticas de criação de sites fantasmas (web farms) e manipulação de links para aumentar artificialmente a relevância de uma página.
- O Google evoluiu e começou a usar o Trust Rank, um algoritmo que identifica sites legítimos e desconta a pontuação de sites suspeitos.
- O Google continuou a atualizar seus algoritmos ao longo do tempo para melhorar a qualidade e a relevância dos resultados de pesquisa.

### Limitações do PageRank e Algoritmo HITS
- O PageRank tinha uma limitação de que uma página poderia ser considerada relevante globalmente, mesmo que não fosse relevante para um determinado tópico específico.
- Surgiu o algoritmo HITS (Hyperlink-Induced Topic Search) em 1999, proposto por Jon Kleinberg, para superar essa limitação.
- O HITS atribui duas pontuações distintas a cada página: uma como "hub" (nó central que aponta para várias outras páginas) e outra como "autoridade" (página que recebe links de vários hubs).
- Hubs são páginas que contêm muitos links para outras páginas, enquanto autoridades são páginas que recebem muitos links de hubs.
- O HITS considera a relevância em um domínio específico ou tópico, em vez de uma pontuação