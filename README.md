
# Banking Service

[![Java](https://img.shields.io/badge/Java-17%2B-orange)](https://www.oracle.com/java/)
[![Quarkus](https://img.shields.io/badge/Framework-Quarkus-blue)](https://quarkus.io/)
[![Maven](https://img.shields.io/badge/Build-Maven-red)](https://maven.apache.org/)
[![PostgreSQL](https://img.shields.io/badge/Database-PostgreSQL-blue)](https://www.postgresql.org/)
[![Apache Kafka](https://img.shields.io/badge/Messaging-Apache%20Kafka-black)](https://kafka.apache.org/)

API REST para gerenciamento de operações bancárias, desenvolvida utilizando **Java e Quarkus**, com foco em integração entre serviços, persistência de dados, mensageria assíncrona e observabilidade.

---

## Sobre o projeto

O **Banking Service** é uma aplicação backend desenvolvida com o objetivo de implementar funcionalidades relacionadas a operações bancárias, utilizando tecnologias modernas do ecossistema Java.

O projeto busca aplicar boas práticas de desenvolvimento de software e conceitos utilizados em arquiteturas de microsserviços, explorando recursos como:

- Desenvolvimento de APIs RESTful.
- Persistência de dados relacionais.
- Integração e comunicação entre serviços.
- Processamento assíncrono de mensagens.
- Serialização e estruturação de eventos.
- Observabilidade e monitoramento da aplicação.

A aplicação utiliza o Quarkus como framework principal, Hibernate ORM with Panache para persistência de dados, PostgreSQL como banco de dados relacional e Apache Kafka para comunicação assíncrona.

## Tecnologias utilizadas

| Tecnologia | Descrição |
|---|---|
| Java | Linguagem principal de desenvolvimento |
| Quarkus | Framework para desenvolvimento backend |
| Maven | Gerenciamento de dependências e build |
| Hibernate ORM with Panache | Persistência e mapeamento objeto-relacional |
| PostgreSQL | Banco de dados relacional |
| REST API | Exposição de serviços e operações |
| REST Client | Comunicação entre serviços |
| Apache Kafka | Mensageria e processamento assíncrono |
| Apache Avro | Serialização de mensagens |
| OpenTelemetry | Instrumentação e observabilidade |

## Arquitetura e conceitos aplicados

O projeto contempla a utilização de conceitos importantes para o desenvolvimento de aplicações backend modernas:

- Arquitetura orientada a serviços.
- APIs RESTful.
- Integração entre aplicações utilizando REST Client.
- Persistência de dados com Hibernate ORM e Panache.
- Comunicação assíncrona utilizando Apache Kafka.
- Serialização de mensagens com Apache Avro.
- Observabilidade utilizando OpenTelemetry.
- Gerenciamento de dependências e automação de build com Maven.

## Pré-requisitos

Antes de executar a aplicação, certifique-se de possuir as seguintes ferramentas instaladas:

- Java em versão compatível com o projeto.
- Maven ou Maven Wrapper.
- PostgreSQL.
- Apache Kafka (necessário para funcionalidades de mensageria).

Também é necessário configurar as propriedades de conexão com os serviços externos no arquivo `application.properties`.

## Executando a aplicação

### 1. Clonando o repositório

```bash
git clone <URL_DO_REPOSITORIO>
```

Acesse o diretório do projeto:

```bash
cd banking-service
```

### 2. Executando em modo desenvolvimento

Para iniciar a aplicação utilizando o modo de desenvolvimento do Quarkus, execute:

```bash
./mvnw compile quarkus:dev
```

No Windows, utilize:

```bash
mvnw.cmd compile quarkus:dev
```

Após a inicialização, a aplicação estará disponível em:

- **API:** http://localhost:8080
- **Quarkus Dev UI:** http://localhost:8080/q/dev/

### 3. Gerando o pacote da aplicação

Para realizar o build e gerar os artefatos da aplicação, execute:

```bash
./mvnw clean package
```

Os arquivos gerados estarão disponíveis no diretório:

```text
target/quarkus-app/
```

Para executar a aplicação empacotada:

```bash
java -jar target/quarkus-app/quarkus-run.jar
```

## Formas de empacotamento

O Quarkus oferece diferentes estratégias de empacotamento e distribuição da aplicação.

### Uber-JAR

Para gerar um único arquivo JAR contendo a aplicação e suas dependências:

```bash
./mvnw package -Dquarkus.package.jar.type=uber-jar
```

Execute o artefato gerado utilizando:

```bash
java -jar target/*-runner.jar
```

### Executável nativo

Também é possível gerar um executável nativo utilizando GraalVM Native Image:

```bash
./mvnw package -Dnative
```

Caso não possua o ambiente GraalVM configurado localmente, a compilação pode ser realizada utilizando um container:

```bash
./mvnw package -Dnative -Dquarkus.native.container-build=true
```

Após a compilação, execute o binário gerado:

```bash
./target/banking-service-1.0.0-SNAPSHOT-runner
```

## Estrutura do projeto

A organização inicial do projeto segue a estrutura padrão de aplicações Quarkus:

```text
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
```

## Documentação oficial

Documentações utilizadas como referência durante o desenvolvimento:

- [Quarkus](https://quarkus.io/guides/)
- [Quarkus REST](https://quarkus.io/guides/rest)
- [Quarkus REST Client](https://quarkus.io/guides/rest-client)
- [Hibernate ORM with Panache](https://quarkus.io/guides/hibernate-orm-panache)
- [Quarkus PostgreSQL](https://quarkus.io/guides/datasource)
- [Quarkus OpenTelemetry](https://quarkus.io/guides/opentelemetry)
- [Apache Kafka](https://kafka.apache.org/documentation/)
- [Confluent Platform](https://docs.confluent.io/)

## Autor

**ghsantos-software**

Projeto desenvolvido com foco no aprendizado e aperfeiçoamento de conhecimentos em desenvolvimento backend com Java, Quarkus, arquitetura de microsserviços, persistência de dados, integração entre serviços e mensageria.

---

**Desenvolvido com Java e Quarkus.**

