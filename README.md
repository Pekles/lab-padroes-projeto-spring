# 🚀 Lab Padrões de Projeto com Spring Boot

Este projeto é o resultado do desafio prático sobre **Padrões de Projeto (Design Patterns)** do bootcamp da **Digital Innovation One (DIO)**. O objetivo da aplicação é gerir um cadastro de clientes integrando dados de endereço consumidos automaticamente a partir de um serviço externo de CEP.

---

## 🛠️ Tecnologias e Ferramentas Utilizadas

* **Java 26**
* **Spring Boot 4**
* **Spring Data JPA** (Persistência de dados)
* **H2 Database** (Banco de dados em memória)
* **OpenFeign** (Cliente HTTP declarativo para integração com API externa)
* **SpringDoc OpenAPI / Swagger UI** (Documentação e testes da API)
* **IntelliJ IDEA**

---

## 📌 Padrões de Projeto Aplicados

1. **Singleton**: Utilizado pelo próprio Spring Framework para gerir a criação de instâncias de *Beans* como `@Service`, `@RestController` e `@Repository`.
2. **Strategy**: Implementado na camada de serviço (`ClienteService`), permitindo alterar a estratégia de persistência e consulta sem acoplar a lógica à camada de apresentação.
3. **Facade**: A camada de controlador (`ClienteRestController`) abstrai a complexidade do sistema, unificando a consulta de CEP externa (ViaCEP) e o salvamento interno no banco de dados H2 sob uma interface REST simples.

---

## 📬 Endpoints da API (CRUD Completo)

A API disponibiliza as seguintes rotas na entidade `/clientes`:

* `GET /clientes`: Lista todos os clientes cadastrados.
* `GET /clientes/{id}`: Busca um cliente específico pelo ID.
* `POST /clientes`: Cadastra um novo cliente (consulta o CEP no ViaCEP e salva o endereço completo).
* `PUT /clientes/{id}`: Atualiza os dados de um cliente existente.
* `DELETE /clientes/{id}`: Remove um cliente pelo ID.

---

## 🏃‍♂️ Como Executar o Projeto

1. Clona o repositório:
   ```bash
   git clone [https://github.com/SEU_USUARIO/lab-padroes-projeto-spring.git](https://github.com/SEU_USUARIO/lab-padroes-projeto-spring.git)
