# Bookstore API de Categorias e Livros

API REST para manter categorias e livros, consultar os títulos de cada categoria e fornecer os dados consumidos pela interface Angular Bookstore. O projeto organiza persistência, regras de serviço, validação e tratamento de erros.

**Categoria:** Backend · API REST.

## Tecnologias principais

- Java 11
- Spring Boot 2.3.7
- Spring Data JPA
- H2
- MySQL

## Recursos da aplicação

- Criar, consultar, atualizar e excluir categorias.
- Criar livros associados a uma categoria.
- Listar os livros de uma categoria.
- Consultar os dados completos de um livro.
- Atualizar e excluir livros, com validação dos dados recebidos.
- Inicializar uma base de demonstração para facilitar a exploração.

## Rotas principais

| Recurso | Operações |
| --- | --- |
| `/categorias` | GET e POST. |
| `/categorias/{id}` | GET, PUT e DELETE. |
| `/livros?categoria={id}` | GET para listagem e POST para criação na categoria. |
| `/livros/{id}` | GET, PUT, PATCH e DELETE. |

Os DTOs das listagens diferem das entidades completas usadas nos detalhes. Os controladores estão em `resources/`, com os serviços, entidades e repositórios nas camadas correspondentes de `src/main/java/`.

## Frontend correspondente

A interface é [Bookstore Frontend](https://github.com/murillomtz/bookstore-front-end), em Angular 11 e Angular Material. As capturas da aplicação integrada estão na galeria desse repositório.

## Executar

Com JDK 11 e o Maven Wrapper:

```bash
./mvnw spring-boot:run
```

No Windows, use `mvnw.cmd spring-boot:run`. A porta padrão é 8080.

O perfil `test`, ativo na configuração original, utiliza H2 e dados de exemplo. O perfil `dev` utiliza MySQL e exige ajuste da conexão em `application-dev.properties`.

Para uma base H2 temporária, sem compartilhar o arquivo de banco com outros exemplos:

```bash
./mvnw spring-boot:run -Dspring-boot.run.arguments="--spring.profiles.active=test --spring.datasource.url=jdbc:h2:mem:bookstore"
```

## Execução para as capturas

A API original foi iniciada com JDK 11, perfil `test` e H2 na porta 8083. O frontend consultou as categorias e os livros da massa de demonstração, incluindo os livros de tecnologia. Não foi usado um mock de API para essas páginas.


## Histórico

Repositório criado no GitHub em **2021-05-03**. Essa data identifica a criação do repositório; não comprova o início nem a conclusão do desenvolvimento.
