---
title: Microsoft SQL Server
tags: [SQL, Estudos, Tecnologia]
style: border
color: primary
description: O Microsoft SQL Server é um sistema gerenciador de Banco de dados relacional (SGBD) desenvolvido pela Sybase em parceria com a Microsoft.
---

O **Microsoft SQL Server** é um sistema de gerenciamento de banco de dados relacional amplamente utilizado. Existem vários comandos importantes no SQL Server que permitem realizar diversas operações no banco de dados. Aqui estão alguns dos principais comandos do SQL Server:

1. **SELECT**: Utilizado para recuperar dados de uma ou mais tabelas. Permite especificar as colunas desejadas, filtros, ordenação e agrupamento.

Exemplo:
```sql
SELECT column1, column2 FROM table_name WHERE condition;
```

2. **INSERT**: Usado para inserir novos registros em uma tabela.

Exemplo:
```sql
INSERT INTO table_name (column1, column2) VALUES (value1, value2);
```

3. **UPDATE**: Utilizado para modificar os valores de um ou mais registros em uma tabela.

Exemplo:
```sql
UPDATE table_name SET column1 = value1, column2 = value2 WHERE condition;
```

4. **DELETE**: Usado para excluir registros de uma tabela.

Exemplo:
```sql
DELETE FROM table_name WHERE condition;
```

5. **CREATE**: Utilizado para criar uma nova tabela, um novo banco de dados ou outros objetos do banco de dados, como índices e procedimentos armazenados.

Exemplo:
```sql
CREATE TABLE table_name (column1 datatype, column2 datatype, ...);
```

6. **ALTER**: Usado para modificar uma tabela existente, adicionando, modificando ou excluindo colunas.

Exemplo:
```sql
ALTER TABLE table_name ADD column_name datatype;
```

7. **DROP**: Utilizado para excluir uma tabela, um banco de dados ou outros objetos do banco de dados.

Exemplo:
```sql
DROP TABLE table_name;
```

Esses são apenas alguns dos comandos básicos do SQL Server. Existem muitos outros comandos e recursos disponíveis para consultas mais complexas, manipulação de dados e administração de banco de dados.