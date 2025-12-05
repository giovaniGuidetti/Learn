**Schemas**
Ao criar um banco de dados do zero, ele já possuirá alguns schemas prontos nele.
Cada schema é responsável por uma funcionálidade presente no banco de dados. A seguir temos as tabelas que vem por padrão no 23ai:

**Schemas para Funcionalidades e Opções Internas (A Maioria)**
* AUDSYS: Controla a infraestrutura de auditoria unificada do Oracle.
* DVSYS: Pertence ao Oracle Database Vault, uma funcionalidade de segurança avançada para controlar o acesso a dados sensíveis.
* LBACSYS: Pertence ao Oracle Label Security, outra funcionalidade de segurança.
* VECSYS: (Novo no 23ai!) Este schema suporta a funcionalidade de AI Vector Search.
* GSMUSER, GGYSYS, etc.: Relacionados a funcionalidades de replicação (GoldenGate) e Sharding.

**Schemas Administrativos**
* PDBADMIN: Um usuário administrativo específico para este Pluggable Database (FREEPDB1).
* SYSBACKUP: Um usuário com privilégios mínimos necessários apenas para realizar backups e recuperações. É uma boa prática de segurança usar este em vez de SYS.
* SYSDG, SYSRAC: Relacionados a tecnologias de alta disponibilidade como Data Guard e Real Application Clusters (RAC).
