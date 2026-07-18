📚 Glossário do Iniciante ao Expert em Banco de Dados


1. SGBD (Sistema de Gerenciamento de Banco de Dados) É o software principal responsável por gerenciar, criar e manipular o seu banco, garantindo segurança e padronização

. O PostgreSQL, por exemplo, é um SGBD do tipo Objeto-Relacional (ORDBMS)
.

2. Dado vs. Informação

Dado: É um valor individual e isolado na sua forma mais básica
.
Informação: É o insight útil, o conhecimento que nós extraímos quando cruzamos e analisamos esses dados (através de consultas)
.

3. Tabelas, Registros e Atributos Quando mapeamos algo do mundo real (como "Aluno"), chamamos de Entidade, que no banco de dados se transforma em uma Tabela

. Essa tabela é formada por Colunas (os atributos ou características, como "Nome" e "Idade") e por Linhas (os registros de cada aluno inserido)
.

4. Chave Primária (Primary Key - PK) É o identificador principal e exclusivo de uma linha na sua tabela

. Funciona como o CPF ou o RG daquele dado; não podem existir dois registros com a mesma chave primária
.

5. Chave Estrangeira (Foreign Key - FK) É a chave usada para ligar uma tabela à outra e implementar relacionamentos

. Se na tabela de "Vendas" houver uma coluna anotando o ID do "Aluno" que comprou, essa coluna é uma Chave Estrangeira
.

6. Normalização É o processo de otimizar as tabelas seguindo regras (as "Formas Normais", como 1FN, 2FN, 3FN)

. Serve para evitar duplicação de dados, acabar com as redundâncias e reduzir a possibilidade de erros de atualização
.

7. SQL (Structured Query Language) e Suas Divisões O SQL é a linguagem padrão que o banco entende

. Ela se divide em subgrupos:

DDL (Data Definition Language): Comandos para criar e alterar a estrutura "física" do banco (ex: CREATE, ALTER, DROP)
.

DML (Data Manipulation Language): Comandos para brincar com os dados em si, como ler, inserir e apagar (ex: SELECT, INSERT, UPDATE, DELETE)
.

DCL (Data Control Language): Comandos de segurança para dar ou tirar permissões de usuários (ex: GRANT)
.

8. Query É o termo em inglês para "Consulta"

. Quando você escreve um comando SELECT para buscar informações, você está rodando uma query
.

9. ACID Uma sigla de ouro! Significa Atomicidade, Consistência, Isolamento e Durabilidade

. O PostgreSQL segue essas regras à risca para garantir que os seus dados permaneçam consistentes e não se corrompam mesmo se acabar a energia ou o servidor quebrar
.

10. Transação É um grupo de comandos no banco de dados tratados como um único bloco, uma operação "tudo ou nada"

. Se alguma operação der erro no meio do caminho, o banco desfaz as alterações para não deixar dados quebrados pela metade
.

11. MVCC (Multi-Version Concurrency Control) O "superpoder" do PostgreSQL para gerenciar a concorrência

. Ele cria "versões" das suas linhas de dados para que os usuários consigam ler um dado ao mesmo tempo que outro usuário está alterando aquele dado, sem que um trave ou bloqueie o outro
.

12. VACUUM Por causa do MVCC, quando você apaga ou altera um dado, o Postgres não o exclui imediatamente, mas cria uma nova versão e deixa a antiga invisível, gerando as chamadas "tuplas mortas"

. O VACUUM atua como um "aspirador de pó" varrendo o banco para limpar esse lixo acumulado, recuperar espaço no disco rígido e devolver a velocidade ao sistema
.

13. Índices (Indexes) Funcionam exatamente como o índice remissivo no final de um livro grosso

. Em vez de o banco ler a tabela linha por linha (uma lentidão enorme), ele olha no índice e vai direto para a página correta buscar a sua informação
.

14. JSONB É um tipo de dado incrivelmente útil e moderno

. Permite que você salve estruturas flexíveis (como em bancos Não-Relacionais / NoSQL) armazenando documentos no formato binário
. Isso economiza tempo, espaço e garante buscas velozes
.

15. Schemas (Esquemas) São como "pastas lógicas" ou "namespaces" criadas para organizar tabelas, funções e visões

. Você pode separar, por exemplo, o departamento financeiro em um esquema e o RH em outro dentro do mesmo banco
.

16. Tablespaces Enquanto o Schema é a organização visual, o Tablespace permite que você diga ao banco de dados exatamente em qual pasta física no seu disco rígido os arquivos pesados das tabelas devem ser guardados

.

17. Views (Visões) e Triggers (Gatilhos)

View: É como uma "foto" ou filtro salvo de uma consulta complexa
. Ela atua como uma tabela virtual, o que facilita o acesso rápido e ajuda no controle de segurança
.

Trigger: Um gatilho disparado para rodar funções e regras de negócio sempre que um evento de alteração acontecer na sua tabela (como durante um INSERT ou DELETE)
.
