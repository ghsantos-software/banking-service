🏦 Banking Service

API REST para gerenciamento de operações bancárias, desenvolvida com Java e Quarkus, utilizando uma arquitetura preparada para integração com serviços externos, persistência de dados e processamento de mensagens.

O projeto tem como objetivo implementar funcionalidades de um serviço bancário, explorando tecnologias modernas do ecossistema Java e conceitos de desenvolvimento de microsserviços.

Tecnologias utilizadas
Java – Linguagem principal.
Quarkus – Framework Java para desenvolvimento de aplicações e microsserviços.
Maven – Gerenciamento de dependências e build.
Hibernate ORM with Panache – Persistência e mapeamento objeto-relacional.
PostgreSQL – Banco de dados relacional.
REST API – Comunicação entre serviços.
REST Client – Integração com serviços externos.
Apache Kafka – Mensageria e comunicação assíncrona.
Apache Avro – Serialização de mensagens.
OpenTelemetry – Observabilidade e rastreamento distribuído.

Pré-requisitos

Antes de executar o projeto, tenha instalado:

Java (versão compatível com o projeto).
Maven ou Maven Wrapper.
PostgreSQL.
Apache Kafka (caso utilize os recursos de mensageria).
⚙️ Executando o projeto
Modo desenvolvimento

Para iniciar a aplicação em modo de desenvolvimento:

bash
./mvnw compile quarkus:dev


A aplicação estará disponível em:

text
http://localhost:8080


O Quarkus também disponibiliza uma interface de desenvolvimento:

text
http://localhost:8080/q/dev/

Build da aplicação

Para gerar o pacote da aplicação:

bash
./mvnw clean package


O artefato será gerado no diretório:

text
target/quarkus-app/


Para executar:

bash
java -jar target/quarkus-app/quarkus-run.jar

Gerando um Uber-JAR

Para empacotar a aplicação em um único arquivo JAR:

bash
./mvnw package -Dquarkus.package.jar.type=uber-jar


Execute com:

bash
java -jar target/*-runner.jar

🐳 Executável nativo

Também é possível gerar um executável nativo utilizando GraalVM:

bash
./mvnw package -Dnative


Caso não tenha GraalVM instalada, utilize a compilação em container:

bash
./mvnw package -Dnative -Dquarkus.native.container-build=true


Execute o binário gerado:

bash
./target/banking-service-1.0.0-SNAPSHOT-runner

📁 Estrutura do projeto
text
banking-service/
├── src/
│   ├── main/
│   │   ├── java/
│   │   │   └── ...
│   │   └── resources/
│   │       └── application.properties
│   └── test/
├── target/
├── pom.xml
├── mvnw
├── mvnw.cmd
└── README.md

📚 Documentação e referências
Quarkus
Quarkus REST
Quarkus REST Client
Hibernate ORM with Panache
Quarkus PostgreSQL
Quarkus OpenTelemetry
Apache Kafka
Confluent Platform

Desenvolvido como projeto de estudo e prática de desenvolvimento backend com Java, Quarkus, microsserviços e tecnologias de mensageria.
