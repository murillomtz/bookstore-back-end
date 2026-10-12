<div align="center">

# Backend da Livraria

</div>

## Sobre o projeto

API para gerenciar livros e categorias de uma livraria, com operações de consulta, criação, edição e remoção.

## Tecnologias principais

- Java
- Spring Boot
- Spring Data JPA
- Maven

## Relação com o frontend

O frontend Angular correspondente está em [Bookstore Front End](https://github.com/murillomtz/bookstore-front-end). Ele consome os recursos de livros e categorias fornecidos por esta API.

## Executar

Com JDK e Maven:

```bash
./mvnw spring-boot:run
```

No Windows, use `mvnw.cmd spring-boot:run`. Confira as configurações em `src/main/resources` para definir o banco de dados e a porta. O frontend possui uma URL de API configurável em seus arquivos de ambiente.

## Interface

O repositório é o backend. Para capturas de tela da interface, consulte o projeto Angular relacionado.
