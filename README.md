Banking Service

API REST para gerenciamento de operações bancárias, desenvolvida com Java e Quarkus.

O projeto tem como objetivo implementar funcionalidades de um serviço bancário, utilizando tecnologias modernas do ecossistema Java, persistência de dados, integração entre serviços e processamento assíncrono de mensagens.

Tecnologias utilizadas
Java
Quarkus
Maven
Hibernate ORM with Panache
PostgreSQL
REST API
REST Client
Apache Kafka
Apache Avro
OpenTelemetry
Pré-requisitos

Antes de executar o projeto, é necessário ter instalado:

Java (versão compatível com o projeto)
Maven ou Maven Wrapper
PostgreSQL
Apache Kafka (para funcionalidades de mensageria)
Executando a aplicação
Modo desenvolvimento

Para iniciar a aplicação em modo de desenvolvimento, execute:

bash
./mvnw compile quarkus:dev


A aplicação estará disponível em:

text
http://localhost:8080


O Quarkus também disponibiliza uma interface de desenvolvimento:

text
http://localhost:8080/q/dev/

Empacotamento e execução

Para gerar o pacote da aplicação, execute:

bash
./mvnw clean package


O artefato será gerado no diretório:

text
target/quarkus-app/


Para executar a aplicação:

bash
java -jar target/quarkus-app/quarkus-run.jar

Gerando um Uber-JAR

Para gerar um único arquivo JAR contendo as dependências da aplicação:

bash
./mvnw package -Dquarkus.package.jar.type=uber-jar


Execute utilizando:

bash
java -jar target/*-runner.jar

Executável nativo

Para gerar um executável nativo utilizando GraalVM:

bash
./mvnw package -Dnative


Caso não tenha GraalVM instalada, é possível realizar a compilação utilizando um container:

bash
./mvnw package -Dnative -Dquarkus.native.container-build=true


Após a compilação, execute:

bash
./target/banking-service-1.0.0-SNAPSHOT-runner

Estrutura do projeto
text
banking-service/
├── src/
│   ├── main/
│   │   ├── java/
│   │   └── resources/
│   │       └── application.properties
│   └── test/
├── target/
├── pom.xml
├── mvnw
├── mvnw.cmd
└── README.md

Guias e documentação
Quarkus
Quarkus REST
Quarkus REST Client
Hibernate ORM with Panache
Quarkus PostgreSQL
Quarkus OpenTelemetry
Apache Kafka
Confluent Platform
Autor

ghsantos-software

Projeto desenvolvido para estudo e prática de desenvolvimento backend utilizando Java, Quarkus, microsserviços, persistência de dados e mensageria.
