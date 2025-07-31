# Sistema de Gerenciamento de Estoque - Backend

Este repositório contém a aplicação backend do Sistema de Gerenciamento de Estoque, desenvolvida com Spring Boot.

## 🚀 Tecnologias Utilizadas

* **Linguagem:** Java 24 (compatível com JDK 17+)
* **Framework:** Spring Boot 3.3.13
* **Banco de Dados:** H2 Database (em memória)
* **ORM:** Spring Data JPA / Hibernate
* **Servidor Web:** Apache Tomcat (embutido)
* **Construção:** Apache Maven
* **Documentação API:** Springdoc-openapi (para Swagger UI)
* **Auxiliar:** Lombok (para redução de boilerplate)

## ✨ Funcionalidades Implementadas

A API oferece os seguintes endpoints para gerenciamento de produtos:

* **Listar todos os produtos:** `GET /api/produtos`
* **Obter produto por ID:** `GET /api/produtos/{id}`
* **Cadastrar novo produto:** `POST /api/produtos`
    * Dados do produto incluem `nome`, `descricao`, `preco`, `quantidade`.
    * `dataCriacao` e `dataAtualizacao` são geradas automaticamente.
* **Atualizar produto existente:** `PUT /api/produtos/{id}`
    * Permite alterar `nome`, `descricao`, `preco`, `quantidade`.
    * Validação: o `preco` não pode ser menor que R$ 9,90.
    * `dataAtualizacao` é atualizada automaticamente.
* **Excluir produto:** `DELETE /api/produtos/{id}`

## ⚙️ Como Inicializar o Backend

Para rodar a aplicação backend em sua máquina local, siga os passos abaixo:

### Pré-requisitos

* Java Development Kit (JDK) 17 ou superior (testado com JDK 24.0.1)
* Apache Maven (já incluído como Maven Wrapper no projeto)

### Passos para Execução

1.  **Clone o repositório:**
    ```bash
    git clone <URL_DO_SEU_REPOSITORIO_BACKEND>
    cd estoque-backend
    ```
2.  **Navegue até o diretório raiz do projeto:**
    Certifique-se de estar na pasta onde o arquivo `pom.xml` está localizado.

3.  **Execute a aplicação Spring Boot:**
    * **No Windows:**
        ```bash
        mvnw.cmd spring-boot:run
        ```
    * **No Linux/macOS:**
        ```bash
        ./mvnw spring-boot:run
        ```

### Endereços Úteis após a Inicialização

* **API REST:** `http://localhost:8080/api/produtos`
* **Documentação Swagger UI:** `http://localhost:8080/swagger-ui.html`
* **Console do Banco de Dados H2:** `http://localhost:8080/h2-console`
    * URL JDBC: `jdbc:h2:mem:stockdb`
    * Usuário: `sa`
    * Senha: password

---
