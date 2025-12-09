# API Web - Biblioteca (Entidade Livro)

[cite_start]Este projeto consiste no desenvolvimento de uma API Web backend para um sistema de gerenciamento de biblioteca, implementando as operações CRUD (Create, Read, Update, Delete) para a entidade **Livro**[cite: 4, 6].

[cite_start]O projeto foi desenvolvido como parte da avaliação da disciplina **Eletiva 01 - Arquitetura e Desenvolvimento Back-end**, ministrada pelo Prof. Danilo Farias[cite: 2].

## 🛠 Tecnologias Utilizadas

[cite_start]Conforme os requisitos técnicos[cite: 15, 26], foram utilizadas as seguintes tecnologias:

* **Linguagem:** TypeScript
* **Ambiente de Execução:** Node.js
* **Framework Web:** Express.js
* **ORM:** TypeORM
* **Banco de Dados:** SQLite (Relacional)

## 🏛 Arquitetura

[cite_start]A solução segue uma arquitetura em camadas ajustada, dividida em[cite: 16]:

1.  [cite_start]**Controller:** Responsável por receber requisições HTTP, validar regras de negócio e chamar o repositório [cite: 18-20].
2.  [cite_start]**Repository:** Responsável pela comunicação direta com o banco de dados e persistência dos dados via ORM[cite: 21, 22].

## 🚀 Como Rodar o Projeto

### Pré-requisitos
* Node.js instalado (ou ambiente GitHub Codespaces).

### Passo a Passo

1.  **Clone o repositório** (ou abra no Codespaces):
    ```bash
    git clone <URL_DO_SEU_REPOSITORIO>
    cd <NOME_DA_PASTA>
    ```

2.  **Instale as dependências:**
    ```bash
    npm install
    ```

3.  **Execute a aplicação:**
    ```bash
    npx ts-node src/index.ts
    ```

4.  O servidor iniciará na porta **3000**.
    * *No Codespaces:* Verifique a aba "PORTS" e abra o endereço local.

## endpoints da API

[cite_start]Abaixo estão listadas as rotas implementadas conforme o exercício[cite: 23, 24]:

| Método | Rota | Descrição |
| :--- | :--- | :--- |
| **POST** | `/api/livros` | Cadastra um novo livro. |
| **GET** | `/api/livros` | Retorna a lista completa de livros. |
| **GET** | `/api/livros/{id}` | Retorna os detalhes de um livro específico. |
| **PUT** | `/api/livros/{id}` | Atualiza informações de um livro existente. |
| **DELETE** | `/api/livros/{id}` | Remove um livro do sistema. |

---

## 📝 Exemplos de Requisição (JSON)

### Estrutura do Objeto (Entidade Livro)
[cite_start]Os campos obrigatórios seguem a definição do cenário de negócio [cite: 8-13].

**Criar Livro (POST)**
```json
{
  "titulo": "Clean Code",
  "autor": "Robert C. Martin",
  "isbn": "978-0132350884",
  "anoPublicacao": 2008,
  "disponivel": true
}
