# Arquitetura Fullstack - Angular & Node.js

Este é um projeto full-stack com um frontend em Angular e um backend em Node.js. O projeto serve como uma base sólida para a construção de aplicações web modernas.

## Visão Geral do Projeto

A aplicação é dividida em duas partes principais:

*   **`server/`**: Um servidor backend construído com Node.js, Express, e TypeScript. Ele utiliza TypeORM para o ORM, `typescript-rest` para criar APIs RESTful, e JWT para autenticação.
*   **`view/`**: Uma aplicação frontend single-page (SPA) construída com Angular 6, TypeScript, e Bootstrap.

## Tech Stack

### Backend (`server/`)

*   **Node.js**: Ambiente de execução JavaScript.
*   **Express**: Framework web para Node.js.
*   **TypeScript**: Superset do JavaScript que adiciona tipagem estática.
*   **TypeORM**: Object-Relational Mapper (ORM) para TypeScript e JavaScript.
*   **typescript-rest**: Biblioteca para criar APIs RESTful usando decorators.
*   **SQLite**: Banco de dados SQL embarcado.
*   **JWT (JSON Web Tokens)**: Para autenticação segura.
*   **Winston**: Biblioteca de logging.
*   **Swagger**: Para documentação da API.

Maiores detalhes em [View Backend](server/README.md)


### Frontend (`view/`)

*   **Angular 6**: Framework para construção de aplicações web.
*   **TypeScript**: Linguagem principal para o desenvolvimento em Angular.
*   **Bootstrap 4**: Framework CSS para design responsivo.
*   **SCSS**: Pré-processador CSS.
*   **ngx-bootstrap**: Componentes Bootstrap para Angular.
*   **Compodoc**: Ferramenta para geração de documentação para projetos Angular.

Maiores detalhes em [View Frontend](view/README.md)

## Pré-requisitos

Antes de começar, certifique-se de ter as seguintes ferramentas instaladas em sua máquina:

*   [Node.js](https://nodejs.org/) (versão 12 ou superior)
*   [NPM](https://www.npmjs.com/) (geralmente vem com o Node.js)
*   [Angular CLI](https://angular.io/cli) (para o frontend)

## Começando

Siga os passos abaixo para configurar e rodar o projeto localmente.

### 1. Clonar o Repositório

```bash
git clone https://github.com/JulioCesar82/arquitetura-fullstack.git
cd arquitetura-fullstack
```

### 2. Configurar o Backend

```bash
cd server
npm install
npm start
```

O servidor backend estará rodando em `http://localhost:3000`.

### 3. Configurar o Frontend

Em um novo terminal:

```bash
cd view
npm install
npm start
```

A aplicação frontend estará disponível em `http://localhost:4200`.

## Scripts Disponíveis

### Backend (`server/`)

*   `npm start`: Inicia o servidor em modo de desenvolvimento com `nodemon`.
*   `npm run build`: Compila o código TypeScript para JavaScript.
*   `npm run lint`: Executa o linter para verificar a qualidade do código.
*   `npm run generate-doc`: Gera a documentação do código com TypeDoc.
*   `npm run generate-doc-api`: Gera a documentação da API com Swagger.
*   `npm run db-migrate`: Executa as migrações do banco de dados.

### Frontend (`view/`)

*   `npm start`: Inicia o servidor de desenvolvimento do Angular.
*   `npm run build`: Compila a aplicação para produção.
*   `npm test`: Executa os testes unitários com Karma.
*   `npm run lint`: Executa o linter do Angular.
*   `npm run e2e`: Executa os testes end-to-end com Protractor.
*   `npm run generate-doc`: Gera a documentação do frontend com Compodoc.

## Documentação

### Documentação da API (Swagger)

Para gerar e visualizar a documentação da API:

1.  Navegue até o diretório `server`.
2.  Execute `npm run generate-doc-api`.
3.  Inicie o servidor com `npm start`.
4.  Acesse `http://localhost:3000/swagger` no seu navegador.

### Documentação do Frontend (Compodoc)

Para gerar e visualizar a documentação do frontend:

1.  Navegue até o diretório `view`.
2.  Execute `npm run generate-doc`.
3.  Execute `npm run serve-doc` para servir a documentação em `http://localhost:4201`.

## Estrutura do Projeto

```
.
├── server/         # Código do Backend (Node.js)
│   ├── config/     # Arquivos de configuração
│   ├── src/        # Código fonte
│   │   ├── app/    # Lógica da aplicação (controllers, services, etc.)
│   │   ├── bootstrap/ # Scripts de inicialização
│   │   └── database/ # Migrações e seeds
│   └── ...
└── view/           # Código do Frontend (Angular)
    ├── src/
    │   ├── app/    # Módulos e componentes do Angular
    │   ├── assets/ # Arquivos estáticos (imagens, etc.)
    │   └── ...
    └── ...
```

## Contribuindo

Contribuições são bem-vindas! Por favor, siga os seguintes passos:

1.  Faça um fork do projeto.
2.  Crie uma nova branch (`git checkout -b feature/nova-feature`).
3.  Faça suas alterações e commit (`git commit -m 'Adiciona nova feature'`).
4.  Envie para a branch original (`git push origin feature/nova-feature`).
5.  Abra um Pull Request.
