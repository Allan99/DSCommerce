# DSCommerce

API REST de e-commerce desenvolvida com **Java** e **Spring Boot**, com persistência via **Spring Data JPA**, banco de dados em memória **H2**, validação de dados e segurança com **Spring Security + OAuth2** (Authorization Server e Resource Server).

> Projeto de estudo baseado no curso Java Spring Professional da [DevSuperior](https://devsuperior.com.br).

## Sumário

- [Tecnologias](#tecnologias)
- [Pré-requisitos](#pré-requisitos)
- [Como executar](#como-executar)
- [Console do H2](#console-do-h2)
- [Testes](#testes)
- [Estrutura do projeto](#estrutura-do-projeto)
- [Autor](#autor)

## Tecnologias

| Tecnologia | Uso |
|---|---|
| Java 25 | Linguagem |
| Spring Boot 4.1.1 | Framework base |
| Spring Web MVC | API REST |
| Spring Data JPA | Persistência / ORM |
| H2 Database | Banco de dados em memória (perfil de teste/desenvolvimento) |
| Spring Validation | Validação de dados de entrada |
| Spring Security | Autenticação e autorização |
| Spring Authorization Server (OAuth2) | Emissão de tokens |
| OAuth2 Resource Server | Proteção dos endpoints com JWT |
| Maven (Maven Wrapper) | Gerenciamento de dependências e build |

## Pré-requisitos

- [JDK 25](https://jdk.java.net/) instalado e configurado no `JAVA_HOME`
- Git

Não é necessário instalar o Maven: o projeto inclui o **Maven Wrapper** (`mvnw` / `mvnw.cmd`).

## Como executar

1. Clone o repositório:

```bash
git clone https://github.com/Allan99/DSCommerce.git
cd DSCommerce
```

2. Execute a aplicação:

```bash
# Linux / macOS
./mvnw spring-boot:run

# Windows
mvnw.cmd spring-boot:run
```

3. A API ficará disponível em `http://localhost:8080`.

### Gerar o build (JAR)

```bash
./mvnw clean package
java -jar target/dscommerce-0.0.1-SNAPSHOT.jar
```

## Console do H2

Com a aplicação em execução, acesse o console do banco em memória:

```
http://localhost:8080/h2-console
```

Use a JDBC URL `jdbc:h2:mem:testdb` (ou a configurada em `application.properties`), usuário `sa` e senha em branco.

## Testes

```bash
./mvnw test
```

## Estrutura do projeto

```
DSCommerce
├── .mvn/wrapper/     # Maven Wrapper
├── src/
│   ├── main/
│   │   ├── java/     # Código-fonte (com.devsuperior.dscommerce)
│   │   └── resources/# Configurações (application.properties, etc.)
│   └── test/         # Testes automatizados
├── mvnw / mvnw.cmd   # Scripts do Maven Wrapper
└── pom.xml           # Dependências e configuração do build
```

## Autor

Feito por [Allan99](https://github.com/Allan99).
