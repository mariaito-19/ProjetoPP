# ProjetoPP — Sistema de Reserva de Laboratórios e Salas

Projeto acadêmico em desenvolvimento no COTUCA. Esta entrega contém cadastros e listagens de salas, laboratórios e usuários, com interface web e API conectada ao SQL Server.

## Tecnologias

Next.js, React, TypeScript, Tailwind CSS, Node.js, Express, SQL Server e bcrypt. Há código inicial de autenticação com JWT.

## Organização

- `frontend/app/`: páginas da aplicação.
- `frontend/componente/`: componentes compartilhados.
- `backend/src/routes/`: rotas HTTP.
- `backend/src/controllers/`: tratamento das requisições.
- `backend/src/models/`: consultas e gravações no banco.
- `backend/src/config/`: conexão com SQL Server.

## Execução local

É necessário Node.js com npm e acesso a um SQL Server com o esquema e as tabelas esperados pelos modelos. O pacote enviado não inclui script de criação do banco.

1. Em `backend`, execute `npm ci`.
2. Copie `.env.example` para `.env` e preencha suas configurações locais.
3. Execute `node server.js` para iniciar a API na porta 8080.
4. Em outro terminal, entre em `frontend`, execute `npm ci` e `npm run dev`.
5. Abra a URL informada pelo Next.js. As páginas usam a API em `http://localhost:8080`.

## Estado desta versão

- O código contém cadastro e listagem de usuários, salas e laboratórios.
- A tela de status ainda é provisória.
- O login está incompleto: `authRoutes.js` está vazio, as rotas não registram autenticação e o método `Usuario.buscarPorLogin` chamado pelo controlador não existe nesta cópia.
- O fluxo de reservas ainda não aparece no código recebido.
- Não há testes automatizados configurados no backend.

Foi feita verificação de sintaxe dos arquivos JavaScript do backend. A integração com banco e a aplicação completa não foram executadas nesta preparação.

As dependências, os arquivos gerados e o `.env` original foram excluídos do pacote para publicação. O código da aplicação foi preservado.
