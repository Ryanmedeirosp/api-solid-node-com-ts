# ApiGymPass

## Descrição

Esta aplicação é um sistema de gerenciamento de academias, permitindo que usuários se registrem, façam check-ins em academias próximas e acompanhem seus históricos de atividades. Com validação de distâncias e autenticação segura, o sistema garante que o usuário esteja dentro do raio de distância permitido para realizar o check-in.

O projeto utiliza tecnologias como Fastify, Prisma e TypeScript, proporcionando uma estrutura leve, rápida e tipagem estática segura para o desenvolvimento backend.

## Funcionalidades

- Registro e autenticação de usuários.
- Realização de check-ins em academias próximas.
- Busca de academias disponíveis.
- Validação de check-ins com base na localização do usuário.
- Histórico de check-ins do usuário.
- Métricas de desempenho e atividades do usuário.

## Tecnologias Utilizadas

- **Node.js**: Ambiente de execução JavaScript no backend.
- **Fastify**: Framework web rápido e eficiente para construir APIs.
- **Prisma**: ORM (Object-Relational Mapping) para interagir com o banco de dados de forma intuitiva e eficiente.
- **TypeScript**: Superset do JavaScript que adiciona tipagem estática ao código, aumentando a segurança e previsibilidade.
- **Zod**: Biblioteca de validação de esquemas para validação robusta de dados.
- **Vitest**: Framework de testes moderno, focado em performance e facilidade de uso.
- **Day.js**: Biblioteca para manipulação e formatação de datas de maneira simplificada.

## Requisitos

Antes de rodar o projeto, certifique-se de ter instalado:

- **Node.js** (versão 16 ou superior)
- **Prisma**: Para conectar e gerenciar o banco de dados.
- Um banco de dados configurado (como PostgreSQL, MySQL ou SQLite).

## Instalação

1. Clone o repositório:
   ```bash
   git clone https://github.com/seu-usuario/seu-repositorio.git
   cd seu-repositorio
   ```

2. Instale as dependências do projeto:
   ```bash
   npm install
   ```

3. Configure o arquivo `.env` com as variáveis de ambiente do seu banco de dados:
   ```env
   DATABASE_URL="url_do_seu_banco_de_dados"
   ```

4. Gere as migrações do banco de dados utilizando Prisma:
   ```bash
   npx prisma migrate dev
   ```

## Como Executar

1. Execute o servidor em modo desenvolvimento:
   ```bash
   npm run dev
   ```

   O servidor será iniciado e estará disponível no endereço `http://localhost:3000`.

2. Para construir o projeto para produção:
   ```bash
   npm run build
   ```

3. Para rodar os testes:
   ```bash
   npm run test
   ```

## Estrutura do Projeto

- **`src/use-case`**: Contém os casos de uso principais da aplicação, como o registro de usuários, busca de academias, e validação de check-ins.
- **`src/utils`**: Funções utilitárias, como o cálculo da distância entre duas coordenadas.
- **`src/errors`**: Definição de erros personalizados usados nos casos de uso, como "credenciais inválidas" ou "usuário já existente".
- **`src/http`**: Lida com as rotas HTTP e lógica de requisição e resposta do Fastify.

## Scripts Disponíveis

- **`npm run dev`**: Inicia o servidor em modo de desenvolvimento.
- **`npm run build`**: Compila os arquivos TypeScript para JavaScript na pasta `build/`.
- **`npm run test`**: Executa a suíte de testes usando Vitest.
- **`npm run test:coverage`**: Executa os testes e exibe a cobertura de código.
- **`npm run prisma:migrate`**: Aplica as migrações do banco de dados usando Prisma.

## Contribuição

Contribuições são bem-vindas! Para contribuir:

1. Faça um fork do projeto.
2. Crie uma nova branch para sua funcionalidade (`git checkout -b feature/nova-funcionalidade`).
3. Commit suas mudanças (`git commit -m 'Adiciona nova funcionalidade'`).
4. Envie para a branch (`git push origin feature/nova-funcionalidade`).
5. Abra um Pull Request.

