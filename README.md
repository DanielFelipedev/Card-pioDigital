🍽️ Cardápio Digital Interativo
Um sistema de cardápio digital moderno e dinâmico, desenvolvido para otimizar a gestão de itens em restaurantes, bares e estabelecimentos de alimentação. Com este projeto, você pode adicionar, editar e remover itens do cardápio em tempo real, proporcionando agilidade e uma melhor experiência para o cliente.

✨ Funcionalidades Principais
Adição de Itens: Interface intuitiva no frontend para incluir novos pratos, bebidas e produtos no cardápio, com detalhes como nome, descrição, preço e categoria.
Edição e Exclusão: Gerencie os itens existentes, atualizando informações ou removendo-os do cardápio instantaneamente, tudo via a interface React.
Visualização Dinâmica: Clientes podem navegar por um cardápio sempre atualizado, com informações precisas e, se implementado, imagens dos produtos.
Pesquisa e Filtragem (Opcional): Capacidade de buscar itens específicos ou filtrar por categorias (ex: entradas, pratos principais, sobremesas).
🚀 Tecnologias Utilizadas
Este projeto é construído com uma arquitetura robusta, dividida em Frontend e Backend:

Frontend
React: Biblioteca JavaScript para construir a interface do usuário interativa e responsiva do cardápio.
Backend
Java: Linguagem de programação principal para a lógica de negócios.
Spring Boot: Framework para o desenvolvimento rápido e eficiente da API RESTful que gerencia os dados do cardápio.
PostgreSQL: Banco de dados relacional robusto e confiável, usado para armazenar todas as informações do cardápio (itens, categorias, etc.).
Ferramentas de Apoio
DBeaver: Ferramenta universal de banco de dados, utilizada para gerenciar, visualizar e interagir diretamente com o banco de dados PostgreSQL.
🛠️ Como Rodar o Projeto
Para configurar e rodar o projeto em sua máquina local, siga os passos abaixo:

Pré-requisitos
Certifique-se de ter instalado em seu ambiente:

Java Development Kit (JDK) 17+: Link para download (ex: OpenJDK)
Maven 3.x: Link para download
Node.js 16+ e npm 8+: Link para download
PostgreSQL: Link para download ou documentação de instalação
DBeaver (Opcional, mas recomendado para gerenciamento): Link para download
1. Clonar o Repositório
Bash

git clone https://github.com/seu-usuario/seu-repositorio.git
cd seu-repositorio
2. Configurar o Banco de Dados PostgreSQL
Crie o Banco de Dados:
Acesse seu servidor PostgreSQL (via psql no terminal ou DBeaver) e crie um novo banco de dados para o projeto.

SQL

CREATE DATABASE cardapio_digital;
Configure as Credenciais no Backend:
No diretório do Backend, localize o arquivo src/main/resources/application.properties (ou application.yml) e configure as credenciais do seu banco de dados.

Properties

# Exemplo para application.properties
spring.datasource.url=jdbc:postgresql://localhost:5432/cardapio_digital
spring.datasource.username=seu_usuario_postgres
spring.datasource.password=sua_senha_postgres
spring.jpa.hibernate.ddl-auto=update # Ou create, create-drop, none (para migrações)
spring.jpa.show-sql=true
spring.jpa.hibernate.ddl-auto=update: Com o Spring Boot e Hibernate, essa configuração geralmente se encarrega de criar as tabelas automaticamente com base nas suas entidades Java. Se preferir controle manual, defina para none e execute scripts SQL.
3. Rodar o Backend (Spring Boot)
Navegue até o diretório do backend:
Bash

cd backend
Construa o projeto com Maven:
Bash

mvn clean install
Execute a aplicação Spring Boot:
Bash

mvn spring-boot:run
O backend estará rodando em http://localhost:8080.
4. Rodar o Frontend (React)
Abra um novo terminal e navegue até o diretório do frontend:
Bash

cd frontend
Instale as dependências do Node.js:
Bash

npm install
Inicie a aplicação React:
Bash

npm start
O frontend estará disponível em http://localhost:3000 (ou outra porta livre, caso a 3000 esteja em uso).
📈 Gerenciamento com DBeaver
O DBeaver é uma ferramenta indispensável para gerenciar e interagir diretamente com o banco de dados PostgreSQL.

Conectar ao Banco de Dados:

Abra o DBeaver.
Clique em "New Database Connection" (ou Ctrl+N e selecione "Database Connection").
Selecione "PostgreSQL".
Preencha os detalhes da conexão (Host, Porta, Banco de Dados: cardapio_digital, Usuário, Senha) que você configurou no application.properties do backend.
Clique em "Test Connection" para verificar se a conexão está funcionando.
Finalize a conexão.
Visualizar e Editar Dados:

No "Database Navigator" (Navegador de Banco de Dados) do DBeaver, expanda sua conexão, depois "Databases" -> cardapio_digital -> "Schemas" -> "public" -> "Tables".
Você verá as tabelas criadas pelo Spring Boot/Hibernate (ex: produto, categoria).
Dê um duplo clique em uma tabela para ver seus dados ou clique com o botão direito para opções como "Open Declaration", "View Data" ou "Generate SQL".
Executar Consultas SQL:

Clique com o botão direito em sua conexão ou banco de dados no DBeaver e selecione "New SQL Editor" (Novo Editor SQL).
Você pode executar comandos SQL para inserir novos itens, atualizar existentes ou consultar dados diretamente no banco de dados.
🤝 Contribuição
Contribuições são sempre bem-vindas! Se você tiver alguma ideia para melhorias ou encontrar bugs, por favor, abra uma issue ou envie um pull request.

📧 Contato
Se você tiver alguma dúvida ou sugestão, sinta-se à vontade para entrar em contato:

[Seu Nome/GitHub/Email]
