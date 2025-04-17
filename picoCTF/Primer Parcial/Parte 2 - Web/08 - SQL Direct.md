## Descripción

Connect to this PostgreSQL server and find the flag!`psql -h saturn.picoctf.net -p 60662 -U postgres pico`Password is `postgres`
## Pistas

1. What does a SQL database contain?

## Solución

`┌──(kali㉿kali)-[~]`
`└─$ psql -h saturn.picoctf.net -p 60662 -U postgres pico`
`Password for user postgres:` 
`psql (17.0 (Debian 17.0-1+b2), server 15.2 (Debian 15.2-1.pgdg110+1))`
`Type "help" for help.`

`pico=# \h`
`Available help:`
  `ABORT                            ALTER SEQUENCE                   CREATE AGGREGATE                 CREATE SUBSCRIPTION              DROP EXTENSION                   DROP TEXT SEARCH PARSER          RESET`
  `ALTER AGGREGATE                  ALTER SERVER                     CREATE CAST                      CREATE TABLE                     DROP FOREIGN DATA WRAPPER        DROP TEXT SEARCH TEMPLATE        REVOKE`
  `ALTER COLLATION                  ALTER STATISTICS                 CREATE COLLATION                 CREATE TABLE AS                  DROP FOREIGN TABLE               DROP TRANSFORM                   ROLLBACK`
  `ALTER CONVERSION                 ALTER SUBSCRIPTION               CREATE CONVERSION                CREATE TABLESPACE                DROP FUNCTION                    DROP TRIGGER                     ROLLBACK PREPARED`
  `ALTER DATABASE                   ALTER SYSTEM                     CREATE DATABASE                  CREATE TEXT SEARCH CONFIGURATION DROP GROUP                       DROP TYPE                        ROLLBACK TO SAVEPOINT`
  `ALTER DEFAULT PRIVILEGES         ALTER TABLE                      CREATE DOMAIN                    CREATE TEXT SEARCH DICTIONARY    DROP INDEX                       DROP USER                        SAVEPOINT`
  `ALTER DOMAIN                     ALTER TABLESPACE                 CREATE EVENT TRIGGER             CREATE TEXT SEARCH PARSER        DROP LANGUAGE                    DROP USER MAPPING                SECURITY LABEL`
  `ALTER EVENT TRIGGER              ALTER TEXT SEARCH CONFIGURATION  CREATE EXTENSION                 CREATE TEXT SEARCH TEMPLATE      DROP MATERIALIZED VIEW           DROP VIEW                        SELECT`
  `ALTER EXTENSION                  ALTER TEXT SEARCH DICTIONARY     CREATE FOREIGN DATA WRAPPER      CREATE TRANSFORM                 DROP OPERATOR                    END                              SELECT INTO`
  `ALTER FOREIGN DATA WRAPPER       ALTER TEXT SEARCH PARSER         CREATE FOREIGN TABLE             CREATE TRIGGER                   DROP OPERATOR CLASS              EXECUTE                          SET`
  `ALTER FOREIGN TABLE              ALTER TEXT SEARCH TEMPLATE       CREATE FUNCTION                  CREATE TYPE                      DROP OPERATOR FAMILY             EXPLAIN                          SET CONSTRAINTS`
  `ALTER FUNCTION                   ALTER TRIGGER                    CREATE GROUP                     CREATE USER                      DROP OWNED                       FETCH                            SET ROLE`
  `ALTER GROUP                      ALTER TYPE                       CREATE INDEX                     CREATE USER MAPPING              DROP POLICY                      GRANT                            SET SESSION AUTHORIZATION`
  `ALTER INDEX                      ALTER USER                       CREATE LANGUAGE                  CREATE VIEW                      DROP PROCEDURE                   IMPORT FOREIGN SCHEMA            SET TRANSACTION`
  `ALTER LANGUAGE                   ALTER USER MAPPING               CREATE MATERIALIZED VIEW         DEALLOCATE                       DROP PUBLICATION                 INSERT                           SHOW`
  `ALTER LARGE OBJECT               ALTER VIEW                       CREATE OPERATOR                  DECLARE                          DROP ROLE                        LISTEN                           START TRANSACTION`
  `ALTER MATERIALIZED VIEW          ANALYZE                          CREATE OPERATOR CLASS            DELETE                           DROP ROUTINE                     LOAD                             TABLE`
  `ALTER OPERATOR                   BEGIN                            CREATE OPERATOR FAMILY           DISCARD                          DROP RULE                        LOCK                             TRUNCATE`
  `ALTER OPERATOR CLASS             CALL                             CREATE POLICY                    DO                               DROP SCHEMA                      MERGE                            UNLISTEN`
  `ALTER OPERATOR FAMILY            CHECKPOINT                       CREATE PROCEDURE                 DROP ACCESS METHOD               DROP SEQUENCE                    MOVE                             UPDATE`
  `ALTER POLICY                     CLOSE                            CREATE PUBLICATION               DROP AGGREGATE                   DROP SERVER                      NOTIFY                           VACUUM`
  `ALTER PROCEDURE                  CLUSTER                          CREATE ROLE                      DROP CAST                        DROP STATISTICS                  PREPARE                          VALUES`
  `ALTER PUBLICATION                COMMENT                          CREATE RULE                      DROP COLLATION                   DROP SUBSCRIPTION                PREPARE TRANSACTION              WITH`
  `ALTER ROLE                       COMMIT                           CREATE SCHEMA                    DROP CONVERSION                  DROP TABLE                       REASSIGN OWNED`                   
  `ALTER ROUTINE                    COMMIT PREPARED                  CREATE SEQUENCE                  DROP DATABASE                    DROP TABLESPACE                  REFRESH MATERIALIZED VIEW`        
  `ALTER RULE                       COPY                             CREATE SERVER                    DROP DOMAIN                      DROP TEXT SEARCH CONFIGURATION   REINDEX`                          
  `ALTER SCHEMA                     CREATE ACCESS METHOD             CREATE STATISTICS                DROP EVENT TRIGGER               DROP TEXT SEARCH DICTIONARY      RELEASE SAVEPOINT`                
`pico=# select * from flags;`
 `id | firstname | lastname  |                address`                 
`----+-----------+-----------+----------------------------------------`
  `1 | Luke      | Skywalker | picoCTF{L3arN_S0m3_5qL_t0d4Y_31fd14c0}`
  `2 | Leia      | Organa    | Alderaan`
  `3 | Han       | Solo      | Corellia`
`(3 rows)`


`picoCTF{L3arN_S0m3_5qL_t0d4Y_31fd14c0}`

## Notas Adicionales



## Referencias
- 

