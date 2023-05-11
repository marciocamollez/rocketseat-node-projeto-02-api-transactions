API de transacoes em fastify. Basicamente cadastra um valor e uma descricao e o seu tipo (crédito ou débito).

Após isso, é capaz de somar os valores das transacoes. Possui testes unitários vitest.

Para realizar os cadastros, fazer via insomnia. Arquivo insomnia.json na raíz

1-Gerar o arquivo de config Typescripy
npx tsc --init

2-Rodar arquivo
npm run dev

3-Criar arquivo lint
.eslintrc.json e inserir abaixo:

{
"extends": ["@rocketseat/eslint-config/node"]
}

4-Verificar se o editor do VSCode (package.json) está com a opcao:
"editor.codeActionsOnSave": {
"source.fixAll.eslint": true
},

5-Verificar erros de lint
npm run lint

6-Criar tabela banco de dados
npm run knex -- migrate:make <nome do banco>

7-Le todas as migrations e executa
npm run knex -- migrate:latest

7-Desfaz a migration que executou
npm run knex -- migrate:rollback

8-Rodar Testes
npm run test
ou
npm test

9-Converter TS em JS para deploy
npm run build
Irá converter e criar uma pasta dist

10-Rodar o projeto convertido
node dist/server.js
