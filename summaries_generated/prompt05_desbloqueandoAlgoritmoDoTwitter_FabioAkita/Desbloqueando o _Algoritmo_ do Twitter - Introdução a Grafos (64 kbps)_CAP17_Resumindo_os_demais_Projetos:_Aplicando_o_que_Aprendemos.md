# Resumo do Capítulo 17 - "Resumindo os demais Projetos: Aplicando o que Aprendemos"

## Real Graph
O Real Graph é um projeto mencionado no arquivo Rhythm e está relacionado ao cálculo da reputação dos usuários do Twitter. O algoritmo de PageRank é utilizado para calcular essa reputação. O PageRank é um algoritmo usado pelo Google para classificar páginas da web de acordo com sua importância.

Exemplo de implementação: Um exemplo de implementação do algoritmo de PageRank no contexto do Twitter seria atribuir um valor de reputação a cada usuário com base em quantas interações positivas (likes, replies, retweets) seus tweets recebem. Quanto mais interações positivas, maior a reputação do usuário.

## Reacos Injector
O Reacos Injector é descrito como um lançador de eventos em stream usado para construir os streams de entrada para serviços baseados em GraphJet. GraphJet é um componente mencionado anteriormente no vídeo.

Exemplo de implementação: O Reacos Injector pode ser usado para gerar eventos em stream relacionados a interações de usuários no Twitter, como likes, replies ou retweets. Esses eventos são coletados e processados pelo GraphJet para fornecer recomendações personalizadas aos usuários.

## Light Ranker
O Light Ranker é um ranqueador mais leve usado pelo índice de pesquisa chamado Early Bird. O Early Bird é mencionado como um projeto legado do Twitter e ainda é usado, sendo construído em cima da biblioteca Lucene.

Exemplo de implementação: O Light Ranker é responsável por classificar os resultados da pesquisa no Twitter de acordo com a relevância. Ele utiliza técnicas de ranqueamento para determinar a ordem em que os tweets serão exibidos nos resultados de pesquisa.

## Heavy Ranker
O Heavy Ranker é mencionado como sendo responsável pela aba "Para você" do Twitter, que exibe uma lista de tweets recomendados aos usuários. Ele utiliza uma rede neural com aproximadamente 48 milhões de parâmetros para prever a relevância de cada tweet candidato.

Exemplo de implementação: O Heavy Ranker recebe cerca de 1500 candidatos de tweets que podem ser relevantes e utiliza uma rede neural treinada para classificá-los com base em interações de tweets, como likes, replies e retweets. O objetivo é otimizar o engajamento positivo dos usuários com os tweets recomendados.

## Trust and Safety
Trust and Safety é mencionado como um projeto relacionado ao TensorFlow, usado para treinar modelos com o objetivo de filtrar conteúdos considerados pornográficos, adultos ou tóxicos.

Exemplo de implementação: O projeto Trust and Safety utiliza o TensorFlow para treinar modelos de Machine Learning capazes de analisar o conteúdo dos tweets e identificar se eles contêm material pornográfico, adulto ou se são considerados tóxicos. Essa filtragem tem o objetivo de manter um ambiente seguro e adequado no Twitter.

## Home Mixer
O Home Mixer é uma coluna mencionada no arquivo Rhythm e possui três fases: Candidate Sourcing, Heavy Ranker e Heurísticas/Filtros.

Exemplo de implementação: O Home Mixer realiza a seleção dos candidatos de recomendação para a aba "Para você" no Twitter. Essa seleção ocorre na fase de Candidate Sourcing, onde diversos filtros são aplicados aos candidatos de tweets para escolher aqueles que podem ser relevantes. Em seguida, os candidatos passam pelo Heavy Ranker, onde são classificados com base em uma rede neural treinada. Por fim, os tweets recomendados passam por heurísticas e filtros adicionais antes de serem exibidos na aba "Para você".

## CR Mixer
O projeto CR Mixer é responsável por mesclar os resultados gerados pelos projetos SimCluster, Real Graph, TNS (Trust and Safety), Tweet Pcred e GraphJets. Esses projetos são responsáveis por filtrar, classificar e fornecer recomendações personalizadas para os tweets.

Exemplo de implementação: O CR Mixer combina os resultados de diferentes projetos para criar uma lista de tweets recomendados na aba "Para você". Os resultados gerados pelos projetos SimCluster, Real Graph, TNS, Tweet Pcred e GraphJets são combinados de acordo com algoritmos específicos para garantir a relevância e diversidade das recomendações.

## In Network e Out of Network
O Twitter gera tweets recomendados na aba "Para você" com base em duas fontes principais: In Network e Out of Network. In Network refere-se aos tweets gerados por pessoas que o usuário segue, enquanto Out of Network refere-se aos tweets gerados por pessoas que o usuário não segue.

Exemplo de implementação: A lista de tweets recomendados na aba "Para você" é composta por uma combinação de tweets gerados pelas pessoas que o usuário segue (In Network) e tweets gerados por outras pessoas que o usuário não segue (Out of Network). O objetivo é fornecer uma mistura de conteúdo familiar e novo para o usuário.

## Visibility Filters
Visibility Filters é um projeto mencionado no contexto do Home Mixer e está relacionado à política de censura do Twitter. Esses filtros são implementados para controlar a visibilidade de certos conteúdos considerados inadequados ou ofensivos.

Exemplo de implementação: Os Visibility Filters são responsáveis por aplicar a política de censura do Twitter, filtrando tweets ou conteúdos que são considerados inapropriados, como spam, conteúdo ofensivo, discurso de ódio, entre outros. Esses filtros garantem que o conteúdo exibido aos usuários esteja em conformidade com as diretrizes de segurança e qualidade do Twitter.

## Naave e Onks
Naave é um projeto mais recente mencionado no vídeo, escrito em Rust. Ele atua como um adaptador para se comunicar com componentes de TensorFlow e PyTorch. Por outro lado, Onks se refere ao Open Neural Network Exchange, um formato de código aberto desenvolvido pela Microsoft e Facebook em 2017 para facilitar a interoperabilidade entre diferentes frameworks de Deep Learning, como PyTorch e TensorFlow.

Ressalvas sobre informações inconsistentes:
- Algumas informações apresentadas no vídeo não são explicadas em detalhes suficientes para fornecer exemplos de implementação precisos.
- A funcionalidade exata e a forma de uso de certos projetos, como Naave e Onks, não são especificadas no vídeo, o que dificulta a elaboração de exemplos detalhados de implementação.