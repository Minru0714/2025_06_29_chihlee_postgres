## 建立資料表的語法

```sql
CREATE TABLE [IF NOT EXISTS] table_name (
   column1 datatype(length) column_constraint,
   column2 datatype(length) column_constraint,
   ...
   table_constraints
);
```

##建立學生資料表的語法,欄位學生ID、name、major

```sql
CREATE TABLE IF NOT EXISTS student(
    student_id SERIAL PRIMARY KEY,
    name VARCHAR(20) NOT NULL,
    major VARCHAR(20) UNIQUE
);
```

##刪除學生資料表的語法

```sql
DROP TABLE IF EXISTS student;
```

##新增1筆資料

```sql
INSERT INTO student (name,major)
VALUES('呂育君','歷史');
```

## 新增多筆資料

```sql
INSERT INTO student (name,major)
VALUES('小柱','生物'),('信忠','英語');
```

##取得資料

```sql
SELECT
  select_list
FROM
  table_name
WHERE
  condition
ORDER BY
  sort_expression;

```

```sql
SELECT student_id, name, major
FROM  student;

SELECT  name, major
FROM  student;

SELECT  *
FROM  student
WHERE name='信忠';

SELECT  *
FROM  student
ORDER BY student_id DESC;

SELECT  *
FROM  student
ORDER BY student_id DESC
LIMIT 3;
```

