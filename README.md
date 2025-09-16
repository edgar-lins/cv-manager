# Gerenciador de Currículos (CV Manager)

O Gerenciador de Currículos é um backend de API GraphQL desenvolvido em Go para gerenciar informações de currículos de forma estruturada e eficiente.

## ✨ Funcionalidades

- **API GraphQL**: Interface moderna e flexível para manipulação dos dados.
- **Operações CRUD para Informações Básicas**:
  - `createBasicInfo`: Cria um novo registro de informações básicas.
  - `basicInfos`: Lista todos os registros.
  - _(Planejado)_: Atualização, deleção e busca por ID.
- **Persistência de Dados**: Utiliza MongoDB para armazenar as informações.

## 🛠️ Tecnologias Utilizadas

- **Linguagem**: Go
- **API**: GraphQL
- **Framework GraphQL**: gqlgen
- **Banco de Dados**: MongoDB
- **Roteador HTTP**: Chi

## 🚀 Como Começar

Siga os passos abaixo para configurar e executar o projeto localmente.

### Pré-requisitos

- Go (versão 1.23 ou superior)
- MongoDB rodando em uma instância local ou remota.

### Configuração

1.  **Clone o repositório:**

```bash
git clone https://github.com/edgar-lins/cv-manager.git
cd cv-manager
```

2.  **Configure as variáveis de ambiente:**

    Crie um arquivo `.env` na raiz do projeto (este arquivo não deve ser versionado).

    ```env
    # Porta para o servidor HTTP
    PORT=8080

    # URL de conexão do MongoDB
    DB_URL=mongodb://localhost:27017

    # Nome do banco de dados
    DB_NAME=cv_manager
    ```

3.  **Instale as dependências:**

```bash
go mod tidy
```

4.  **(Opcional) Gere o código GraphQL:**

    Se houver alterações nos arquivos de schema (`.graphqls`), execute o comando abaixo para atualizar o código gerado pelo `gqlgen`.

```bash
go run github.com/99designs/gqlgen generate
```

5.  **Execute a aplicação:**

    ```bash
    go run server.go
    ```

6.  **Acesse o Playground:**

    A aplicação estará rodando e o GraphQL Playground estará acessível em:
    http://localhost:8080/

## Créditos

Este projeto foi criado acompanhando um tutorial em vídeo no YouTube.  
**Agradecimentos especiais ao canal [Arthur 404 dev](https://www.youtube.com/@Arthur404dev) pela orientação e inspiração.**

---

Sinta-se à vontade para contribuir ou sugerir melhorias!
