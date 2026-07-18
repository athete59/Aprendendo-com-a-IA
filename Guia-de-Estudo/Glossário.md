# 📚 Glossário do Iniciante ao Expert em Banco de Dados

## 1. SGBD (Sistema de Gerenciamento de Banco de Dados)
É o software principal responsável por gerenciar, criar e manipular o seu banco, garantindo segurança e padronização. O PostgreSQL, por exemplo, é um SGBD do tipo Objeto-Relacional (ORDBMS).

## 2. Dado vs. Informação
* **Dado:** É um valor individual e isolado na sua forma mais básica (como um número ou texto em uma planilha).
* **Informação:** É o insight útil, o conhecimento que nós extraímos quando cruzamos e analisamos esses dados através de consultas.

## 3. Tabelas, Registros e Atributos
Quando mapeamos algo do mundo real, chamamos de Entidade, que no banco de dados se transforma em uma **Tabela**. Essa tabela é formada por **Colunas** (os atributos ou campos com tipos de dados específicos, como "Nome" e "Idade") e por **Linhas** (os registros individuais inseridos na tabela).

## 4. Chave Primária (Primary Key - PK)
É o identificador principal e exclusivo de uma linha na sua tabela. Funciona como o CPF ou o RG daquele dado; identifica as informações de forma única, logo, não podem existir dois registros com a mesma chave primária.

## 5. Chave Estrangeira (Foreign Key - FK)
É a chave usada para ligar uma tabela à outra e implementar relacionamentos. Se na tabela de "Vendas" houver uma coluna anotando o ID do "Curso" que foi vendido, essa coluna é uma Chave Estrangeira conectando as informações do curso correspondente.

## 6. Normalização
É o processo de otimizar as tabelas aplicando técnicas para reduzir redundâncias, duplicações e inconsistências nos dados. A Primeira Forma Normal (1FN), por exemplo, exige que uma coluna não possua atributos multivalorados (ou seja, nunca guarde vários telefones misturados no mesmo campo).

## 7. SQL (Structured Query Language) e Suas Divisões
O SQL é a linguagem padrão desenvolvida para definir, manipular e controlar o acesso a dados de bancos relacionais. Ela se divide em subgrupos:
* **DDL (Data Definition Language):** Comandos para criar, alterar e eliminar a estrutura física dos objetos do banco (ex: `CREATE`, `ALTER`, `DROP`).
* **DML (Data Manipulation Language):** Comandos para acessar, inserir, alterar e excluir os dados em si (ex: `SELECT`, `INSERT`, `UPDATE`, `DELETE`).
* **DCL (Data Control Language):** Comandos de segurança usados para controlar o acesso aos dados, dando ou tirando permissões de usuários (ex: `GRANT`).

## 8. Query
É o termo em inglês para "Consulta". Quando você escreve um comando para buscar informações específicas, você está rodando uma query.

## 9. MVCC (Multi-Version Concurrency Control)
É o mecanismo de controle de concorrência do PostgreSQL. Em vez de travar o banco para leitura enquanto alguém salva um dado novo, ele cria "versões" das suas linhas de dados (instantâneos) para que as operações de leitura nunca bloqueiem as operações de escrita, otimizando ambientes de alta concorrência.

## 10. VACUUM
Por causa do MVCC, quando você apaga ou altera um dado, o Postgres não o exclui imediatamente do disco, mas cria uma nova versão e deixa a antiga invisível, gerando as chamadas "tuplas mortas". O processo de manutenção sistemático `VACUUM` atua varrendo o banco para limpar esse lixo acumulado e evitar a lentidão (bloat) do sistema.

## 11. Índices (Indexes)
São estruturas otimizadas criadas para aumentar a velocidade de busca e a performance de um banco de dados de grande escala. Funcionam como um índice de livro, e existem em vários tipos para diferentes necessidades, como B-tree (o padrão), GIN e Hash.

## 12. JSONB
É um tipo de dado avançado que converte documentos JSON textuais em um formato binário decomposto dentro do PostgreSQL. Embora tenha um leve custo de tempo na hora de salvar, oferece vantagens gigantescas em termos de performance de consulta e eficiência de armazenamento para dados flexíveis.

## 13. Schemas (Esquemas)
São como "pastas lógicas" (namespaces) que contêm objetos nomeados como tabelas, visões e funções. Eles servem para organizar o banco de dados e simplificar o gerenciamento de permissões (por exemplo, separar módulos de um aplicativo ou departamentos de uma empresa sem misturar tudo).

## 14. Tablespaces
Permitem que os administradores definam exatamente em qual espaço de diretório ou pasta física no disco rígido os arquivos do banco de dados e suas tabelas serão efetivamente guardados.

## 15. Views (Visões) e Triggers (Gatilhos)
* **View:** Uma consulta SQL salva que atua e pode ser consultada como se fosse uma tabela virtual no banco de dados.
* **Trigger:** Um gatilho programado para ser disparado automaticamente a partir de um evento no banco de dados, como uma exclusão (`DELETE`), inserção (`INSERT`) ou alteração (`UPDATE`).
```
