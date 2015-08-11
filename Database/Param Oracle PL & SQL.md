#Pl-SQL-General


  <style>
   

td, th {
    border: 1px solid black;
    padding: 5px;
}

table {
    border-collapse: collapse;
    
}
  </style>
  

|   |  |  |  | 
|  ----| ----| ----| ----| 
|   PL/SQL |  it is interpreted and operating system Independent like Java programing environment |   |   |   
|    |  it started its life around 1980. |   |   |   
|    |  after oracle 9i release 2, PL/SQL is both procedural and OOPs language |   |   |   
|    |  it is case-insenstive language |   |   |   
|    |  PL / SQL is extend from ADA language, which itself extend from Pascal language |   |   |   
|    |  As a PL / SQL developer, we should be familiar with most of built-in packages. It s like library |   |   |   
|    |  PL/SQL version is same as oracle product version like 10.2, 11.1,11.2 and etc. |   |   |   
|    |   |   |   |   
|   c |  **Structured Programming** |   |   |   
|   Java |  *OOPs programming* |   |   |   
|   ETL |  Component Oriented Programming |  version |  procedure |   
|   PL/sql |  Block/Structured oriented Programming |  object type |  native code |   
|    |   |  external |   |   
|    |  PL/SQL General |   |   |   
|    |  function/pricdure/block intro |   |   |   
|    |  11g new feature |   |   |   
|    |  10 g new feature |   |   |   
|    |   |   |   |   

#DataType


|   |  |  |  | 
|  ----| ----| ----| ----| 
|   **Base Type** |  **SubType / Intermediate Base Type** |  **SubType** |  **Globalization** |   
|   VARCHAR2 |  VARCHAR, STRING |  NVARCHAR2 |  |   
|   CHAR |  CHARACTOR |  NCHAR |  |   
|   |  |  |  |   
|   ROWID, UROWID |  |  |  |   
|   |  |  |  |   
|   LANG,LANG RAW |  |  |  |   
|   |  |  |  |   
|   DATE |  INTERVAL DAY TO SECOND,  INTERVAL YEAR TO MONTH |  |  |   
|   TIMESTAMP |  TIMESTAMP[(precision)] WITH TIME ZONE |  |  |   
|   |  |  |  |   
|   BINARY_INTEGER[OR]/ PLS_INTEGER |  NATURAL, POSITIVE, NATURALN, POSITIVEN, SIGNTYPE, SIMPLE_INTEGER |  |  |   
|   BINARY_DOUBLE |  **SIMPLE_DOUBLE** |  IEE-754  data type |  |   
|   BINARY_FLOAT |  **SIMPLE_FLOAT** |  IEE-754  data type |  |   
|   NUMBER |  DEC, DECIMAL, NUMERIC |  fixed point |  |   
|   INTEGER, INT, SMALLINT |  |  |  |   
|   REAL |  Floating-point |  |  |   
|   DOUBLE PRECISION |  Floating-point |  |  |   
|   FLOAT |  Floating-point |  |  |   
|   |  |  |  |   
|   BFILE |  |  |  |   
|   BLOB |  |  |  |   
|   CLOB |  |  |  |   
|   NCLOB |  |  |  |   


#composite types

|   |  |  |  |  |  |  | 
|  ----| ----| ----| ----| ----| ----| ----| 
|   Record structure ( PLSQL only) |  TYPE employeeRecord IS RECORD (x number,y varchar2(23)); |  |  |  |  |  |   
|   Varray ( SQL and PLSQL ) |  [CREATE OR REPLACE] TYPE myNumbers IS/AS VARRAY (20) OF NUMBER; |  fixed size of element |  |  |  |  |   
|   Nested Table. ( SQL and PLSQL ) |  [CREATE OR REPLACE]TYPE ordinalCollection IS TABLE OF VARCHAR2 (30); |  variable size of element |  |  |  |  |   
|   Associated Array ( PLSQL only) |  [CREATE OR REPLACE TYPE] type_name AS TABLE OF element_type [ NOT NULL ] [OR]INDEX BY [ PLS_INTEGER | BINARY_INTEGER | VARCHAR2(size) ]; |   |  |  |  |  |   
|   reference cursor |  TYPE ref_cursor IS REF CURSOR [RETURN { catalog_row | record_structure }] |   |  |  |  |  |   
|    |  |  |  |  |  |  |   
|    |   |   |   |  |  |  |   
|   collection API |  Introduced in Oracle 8i |  |  |  |  |  |   
|   SIZE |   |   |  |  |  |  |   
|   LIMIT |  total size of array |  used only  in varray |  |  |  |  |   
|   COUNT |  no. of element Initialized in collection |  **used in both varray and nested table** |  |  |  |  |   
|   EXTEND |  allocate SPACE for one or more element |  used in varray and nested table |  i cannot call extend method on same array continously. it will give error. so, extend-assignvalue-then-extend.. |  i must initialize at least as empty for varray and nested table before to call EXTEND method. otherwise i will get error. i tested |  |  |   
|   TRIM |  deallocate  SPACE for one or more elements |  |  |  |  |  |   
|   DELETE |  delete one or more element |  |  |  |  |  |   
|   EXISTS |  to check a element in collection |  |  |  |  |  |   
|   CAST |  use to cast varray to nested table |  |  |  |  |  |   
|   LAST |  highest index of collection |  used in varray and nested table associative array |  |  |  |  |   
|   FIRST |  lowest index of collection |  used in varray and nested table associative array |  |  |  |  |   
|   NEXT |  return next index or false |  used in varray and nested table associative array |  |  |  |  |   
|   PRIOR |  previous index or false |  used in varray and nested table associative array |  |  |  |  |   
|    |   |   |   |  |  |  |   
|   collection set operator |  CARDINALITY |  I can use these set operator in IF statement. only for scala typed varray or nested table |  |  |  |  |   
|   EMPTY |   |  |  |  |  |  |   
|   MEMBER OF |  |  |  |  |  |  |   
|   MULTISET EXCEPT |  |  |  |  |  |  |   
|   MULTISET INTERSECT |  |  |  |  |  |  |   
|   MULTISET UNION |  |  |  |  |  |  |   
|   SET |  |  |  |  |  |  |   
|   SUBMULTISET |  |  |  |  |  |  |   
|    |   |   |   |  |  |  |   
|   collection exception( 5 ) |  |  |  |  |  |  |   
|   COLLECTION_IS_NULL |  |  |  |  |  |  |   
|   NO_DATA_FOUND |  used in associative array |  |  |  |  |  |   
|   SUBSCRIPT_BEYOND_COUNT |  used in varray and nested table |  |  |  |  |  |   
|   SUBSCRIPT_OUTSIDE_LIMIT |  used in varray and nested table |  |  |  |  |  |   
|   VALUE_ERROR |  |  |  |  |  |  |   
|   |  |  |  |  |  |  |   
|   ``` **composite data type** |  **is Object Type** |  **is available for SQL** |  **is available for PL-SQL** |  **fixed Size** |  **can use Object or record** |  **remove element** |   
|   **Record** |  no |  no |  yes |  N/A |  N/A |  N/A |   
|   **Varray** |  yes |  yes |  yes |  yes |  yes |  No |   
|   **Nested Table** |  yes |  yes |  yes |  no |  yes |  Yes |   
|  ``` **associated Array** |  no |  no |  yes |  no |  yes |  Yes |  