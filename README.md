# MVC_IanPereira
Aqui postarei toda a estruturação do MVC do nosso website com Sails.js

# Readme

- Nome do Projeto: MVC da aba de perfil
- Descrição: Nesse projeto desenvolvi uma arquitetura MVC com objetivo de estruturar o back-end do perfil de usuário, e dessa forma adicionar métricas, postagens e informações do mesmo na aba perfil.
- Arquitetura: MVC (Model-View-Controller)
- Ferramenta de Diagramação: draw.io

### Modelos (Models):
- As entidades são respectivamente usuário: o que utiliza a plataforma, podendo ser tanto uma instituição como pessoas comum, posts: postagens no perfil dos usuários e no feed 
- Um usuário pode ter vários posts que respectivamente tem seus atributos como id e conteúdo.
### Controladores (Controllers):
- Dentro da categorias de controladores temos: User e post, cada um com métodos para remover, adicionar, procurar e listar informações.
- No controlador de user, estao presentes os seguintes métodos: Listar, gravar, deletar e procurar, a partir do seu uso se tornará possível filtrar postagebs de usuário, trocar informações de um post, deletá-lo e adicionar novos posts.
- Os controladores são as ferramentas disponíveis para usuário para que ele requisite ações dentro da plataforma, eles são quem interpretam os inputs do users, por sua vez, os models recebem estas informações e mudam seu estado a partir do que foi pedido pelo usuário, após isso, essas mudanças são enviadas para o view que apresenta o resultado de um request ao user.

### Views (Views):
- Dentre as Views estão: Header, que mostra informações de menu do website e apresenta uma forma de navegação simplificada; Perfil do usuário, que apresenta o nome, foto, e informações básicas que compõe a identidade do usuário; Publicações que mostra todas as publicação daquele respectivo user.

### Infraestrutura:

- Será utilizado no projeto MySql e a framework Sails.js para estruturação do back-end
- A partir do sails.js a conexão com o banco de dados pode ser feita de maneira relativamente simples, já que MySql é open-source, a partir disso, seriam criadas tabelas relativas à cada atributo e as conexões entre tabelas poderiam ser feitas a partir de chaves estrangeiras.


#### Implicações da Arquitetura:
Com a estruturação MVC, o projeto está preparado para escalar de forma eficiente. A separação clara entre modelos, visualizações e controladores permite que diferentes partes do sistema sejam modificadas e expandidas independentemente, facilitando a adição de novos recursos e funcionalidades conforme o projeto cresce.

A arquitetura MVC promove a manutenção do código de forma mais organizada. Como cada componente tem uma responsabilidade específica, é mais fácil localizar e corrigir problemas, além de facilitar a adição de novos recursos sem interferir no funcionamento existente.

A separação de preocupações da arquitetura MVC também beneficia a testabilidade do projeto. Com modelos, visualizações e controladores claramente definidos, é mais simples escrever testes unitários e de integração para garantir que o sistema funcione conforme o esperado em diferentes cenários.

### Recursos Adicionais:
Documentação do Sails.js: https://github.com/balderdashy/sails
Tutorial do draw.io: https://m.youtube.com/watch?v=w3zm-wbmlpc
Exemplos de diagramas MVC: https://www.lucidchart.com/pages/templates
MySQL documentação: https://docs.oracle.com/en-us/iaas/mysql-database/doc/getting-started.html
