**Ao criar um banco de dados oracle, dois usuários importantes são criados junto a ele.**

**Usuários:**
* sys
* system

**sys (Usuário principal e todo poderoso)**
Pode ser conectado usando dois privilégios distintos, **SYSOPER** e **SYSDBA**. 
* Dono do Dicionário de Dados: A função mais importante do SYS é ser o proprietário do Dicionário de Dados (Data Dictionary). O dicionário é um conjunto de tabelas e views internas (como V$INSTANCE, DBA_TABLES, DBA_USERS, etc.) que contêm os metadados sobre o banco de dados: quem são os usuários, quais tabelas existem, onde os arquivos estão, etc. O banco de dados usa essas tabelas o tempo todo para funcionar.
* Regra de Ouro: Nunca, jamais, crie tabelas ou objetos de aplicação no schema do SYS. Fazer isso é considerado um erro gravíssimo que pode corromper o dicionário de dados e tornar o banco de dados irrecuperável.
* SYSDBA - O privilégio SYSDBA concede controle total sobre a instância do banco de dados e o banco de dados em si.
* SYSOPER - O privilégio SYSOPER é mais restrito, projetado para um operador que realiza tarefas operacionais básicas, mas não deve ter acesso ao conteúdo dos dados dos usuários. 

**system**
É uma conta administrativa de alto nível usada para tarefas de administração de banco de dados.
* Administrador Padrão: Ele é criado com um conjunto robusto de privilégios de DBA (mas menos que SYS). É a conta destinada a realizar tarefas administrativas do dia a dia.
* Uso: A principal função do SYSTEM (do ponto de vista de um desenvolvedor) é ser a conta usada para criar outros usuários, roles (grupos de permissões) e tablespaces (espaços de armazenamento).
* Regra de Ouro: Assim como SYS, você não deve criar objetos de aplicação no schema do SYSTEM. Use o SYSTEM para preparar o ambiente para os desenvolvedores, mas não para o desenvolvimento em si.
