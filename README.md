 Sistema de Controle de Reembolso de Frota (fuelrequest)

Este projeto contém o banco de dados e as consultas SQL para gerenciar os reembolsos de quilometragem e combustível da frota de veículos.


 
   Estrutura do Banco de Dados



O banco de dados `fuelrequest` é composto pelas seguintes tabelas principais:

| Tabela | Descrição |
| :--- | :--- |
| **`reembolso`** | Registros de cada solicitação de reembolso, incluindo datas e quilometragem. |
| **`motorista`** | Cadastro dos motoristas e suas CNHs. |
| **`veiculo`** | Informações sobre os veículos, como marca, modelo e placa. |
| **`admfrota`** | Cadastro dos administradores responsáveis pela frota. |

 
   Conteúdo do Repositório (Scripts SQL)



O projeto está organizado nos seguintes scripts SQL:

criandotabelas.sql

      Contém os comandos DDL (CREATE TABLE) que definem o esquema do banco de dados5. Estabelece as chaves primárias e as chaves estrangeiras (FOREIGN KEY) entre as tabelas6.

INSERTS.sql

      Contém os comandos DML (INSERT INTO) para popular as tabelas iniciais com dados de exemplo (motoristas, veículos, administradores e os primeiros reembolsos)7.

JOINSEFILTROS.sql

      Contém consultas complexas (SELECT) que demonstram a interação entre as tabelas (usando JOINs), filtros (WHERE), e cálculos de quilometragem percorrida e valor de reembolso8.
      Cálculo do Reembolso: Utiliza a lógica de $10\text{ km/L}$ de consumo médio e $R\$ 6,79\text{/L}$ para o valor da gasolina na consulta principal9.

UPDATE_E_DELETE.sql

      Contem os comandos DML (UPDATE e DELETE) para modificar e remover dados específicos no banco de dados, utilizando condições (WHERE).


O arquivo de banco de dados fuelrequest.sqlite.
