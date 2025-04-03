#Support-Tickets-NodeJs.
 
Desenvolvimento de uma API do zero para gerenciar tickets de suporte técnico. A API permitirá criar, atualizar, listar e filtrar tickets, além de fechar e excluir tickets.
Os dados enviados nas requisições incluem informações sobre equipamento, descrição e nome do usuário.

- Foi utilizado o Insomnia para enviar as requisições.
![tela1](https://github.com/user-attachments/assets/baaaed2e-91aa-493a-b6b5-e35544969a05)

____________________________________________________________________________________________________________________________________________________________________________________________________________________
____________________________________________________________________________________________________________________________________________________________________________________________________________________
-------> Iniciado o Projeto:

  ----------| Configurações: |-----------

- Iniciado o servidor.
- Criado um middleware para manipular o conteúdo das requisições chamado jsonHandler.js: é exportada uma função assíncrona que lida com o corpo das requisições, convertendo para JSON.
O middleware é essencial para processar e manipular dados enviados nas requisições HTTP.

  ----------| Rotas, Middleware e Controller: |-----------
  
- Criado uma lista de rotas para organizar a API com um arquivo tickets.js para separar as rotas relacionadas aos tickets.
- Exportado uma constante com a estrutura de uma rota, incluindo um método, um path e um controller. 
- Criado um objeto de ticket, utilizando a rota "barra tickets" com o método "post". Foram detalhadas as informações necessárias, como equipamento, descrição e nome do usuário.
- REcuperado as informações no controller e implementado um identificador único para cada ticket usando o node:crypto, biblioteca nativa do node.
- Definido de um status padrão "open" e a inclusão de datas de criação e atualização.
  
  ----------| Banco de dados e parâmetros: |-----------

- É desenvolvido um arquivo "database.js" para manipular o banco de dados, utilizando o módulo file system do Node.js.
- criados métodos para inserir e selecionar dados, além de um método de persistência.
- criado um método de inserção de dados, verificando se a tabela já existe. Caso exista, os novos dados são adicionados à tabela. Se não existir, é criado o primeiro registro.
- processo de listar tickets cadastrados em um banco de dados. Foi criado um método de select para buscar os dados no banco, um novo controller chamado index.js para listar os tickets e a importação desse controller na rota de tickets.
- A API valida parâmetros nomeados e não nomeados nas requisições.
- Os parâmetros são tratados, extraidos e separandos em chave e valor.
- Aplicado filtros em uma requisição no banco de dados para verificar a existência deles e como aplicá-los na consulta.
- Criado um método de atualização de registros em um banco de dados.
- atualizar o status de um ticket no banco de dados sem a necessidade de criar um novo método.
- Criado uma rota para deletar um ticket em uma aplicação.
  
----------| Requisições: |-----------

- CREATE (Criação dos dados)
- INDEX  (Obter/listar os dados)
- UPDATE (Atualizar os dados)
- CLOSE (Atualizar o parâmetro de status)
- REMOVE (Deletar os dados)

____________________________________________________________________________________________________________________________________________________________________________________________________________________
____________________________________________________________________________________________________________________________________________________________________________________________________________________

Tecnologias: JAVASCRIPT. NODEJS.




 
 
