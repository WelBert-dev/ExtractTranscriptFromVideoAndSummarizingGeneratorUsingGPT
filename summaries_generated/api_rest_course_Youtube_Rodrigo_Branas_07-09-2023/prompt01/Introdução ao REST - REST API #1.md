## Resumo da vídeo aula "Introdução ao REST - REST API #1" - Rodrigo Branas

Nesta vídeo aula, Rodrigo Branas introduz os fundamentos do REST (Representational State Transfer) e explora os conceitos, paradigmas e histórico relacionados à API REST. O vídeo aborda o desenvolvimento de APIs seguindo boas práticas de programação, como DDD (Domain Driven Design), Ports & Adapters Architecture, Arquitetura Hexagonal, Design Patterns e TDD (Test Driven Development). A série promete cobrir tópicos como métodos HTTP, códigos de retorno, segurança, monitoramento, performance e alternativas ao REST.

### API (Application Programming Interface)

- API é uma interface de programação que permite interações programáticas entre sistemas.
- Não se limita às web APIs, existem APIs em bibliotecas e frameworks.
- APIs facilitam a colaboração entre sistemas.

### Evolução das Integrações

- Antes das web APIs, havia tecnologias como EDI (Electronic Data Interchange), DeCon, Corba e RMI.
- XML-RPC e SOAP foram usados para integração de sistemas antes da ascensão do REST.

### Web e REST

- A ascensão do AJAX permitiu aplicações web mais dinâmicas e ricas em experiência do usuário.
- Jesse James Garrett introduziu o conceito de AJAX em 2005.
- Separar o front-end do back-end impulsionou o desenvolvimento de web APIs.
- JSON ganhou popularidade como alternativa mais simples ao XML.
- O conceito de REST foi definido por Roy Fielding em sua tese de doutorado em 2000.

### Restrições Arquiteturais do REST

1. **Client-Server**: A separação entre cliente e servidor permite a evolução independente de ambas as partes.
2. **Stateless**: Não há estado retido entre as requisições; cada uma é independente.
3. **Layered System**: As requisições passam por várias camadas intermediárias.
4. **Cacheable**: As respostas podem ser cacheadas para melhorar a escalabilidade e o desempenho.
5. **Uniform Interface**: Uma interface uniforme que identifica recursos e permite manipulação por meio da representação dos recursos.
6. **Self-Descriptive Messages**: As mensagens devem conter informações suficientes para serem interpretadas e processadas.
7. **Hypermedia as the Engine of Application State (HATEOAS)**: As mensagens devem conter links que orientam a navegação e a transição de estados da aplicação.

### Níveis de Maturidade do REST

- Richardson Maturity Model descreve os níveis de maturidade do REST, indo do nível 0 (pouco restrito) ao nível 3 (totalmente restrito).

### Limitações do REST

- REST pode levar a problemas de over-fetching ou under-fetching de dados para diferentes clientes.
- Alternativas como BFF (Back End for Front End), GraphQL e gRPC são usadas para abordar essas limitações.
- REST é poderoso para criar APIs simples e reutilizáveis, suportando o crescimento de sistemas.

Nesta série, os tópicos futuros incluirão segurança, monitoramento, documentação e exemplos práticos, além de explorar alternativas ao REST.