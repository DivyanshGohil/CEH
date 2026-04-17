

### In which of the following SQL injection attacks does an attacker deface a web page, insert malicious content into web pages, or alter the contents of a database?

- Authorization bypass
- **Compromised data integrity**
- Remote code execution
- Compromised availability of data

> Explanation:

> **Authorization Bypass**: Using this attack, an attacker alters authorization information stored in the database by exploiting an SQL injection vulnerability.

> **Compromised Data Integrity**: Using this attack, an attacker defaces a web page, inserts malicious content into web pages, or alters the contents of a database.
    
> **Remote Code Execution**: Using this attack, an attacker compromises the host OS.
    
> **Compromised Availability of Data**: Using this attack, an attacker deletes the database information, delete logs, or audit information stored in a database.



### In which of the following attacks does an attacker pose a true or false question to an database to determine whether an application is vulnerable to SQL injection?


- **Blind SQL injection**
- Error-based SQL injection
- In-band SQL injection
- Union SQL injection

> Explanation:

    
> **Union SQL Injection**: In a UNION SQL injection, an attacker combines a forged query with a query requested by the user using a UNION clause.
    
> **Blind/Inferential SQL Injection**: In blind SQL injection, an attacker poses a true or false question to the database to determine whether the application is vulnerable to SQL injection.
    
> **Error-based SQL injection**: In this type of SQL injection, the attacker forces the database to return error messages in response to his/her inputs. Later, the attacker may analyze the error messages obtained from the underlying database to gather information that can be used for constructing the malicious query.
    
> **In-band SQL injection**: In in-band SQL injection, attackers use the same communication channel to perform the attack and retrieve the results.




### In which of the following attacks does an attacker use a conditional OR clause in such a way that the condition of the WHERE clause will always be true?


- **Tautology**
- End-of-line comment
- Illegal/logically incorrect query
- UNION SQL injection

>Explanation:

    
> In a **UNION SQL injection**, an attacker uses a UNION clause to append a malicious query to the requested query. 

> An attacker may gain knowledge by injecting illegal/logically incorrect requests such as injectable parameters, data types, names of tables, and so on.
   
> In a **tautology-based SQL injection** attack, an attacker uses a conditional OR clause in such a way that the condition of the WHERE clause will always be true.
    
> In **end-of-line SQL injection**, an attacker uses Line comments in specific SQL injection inputs. 



### In which of the following attacks does an attacker inject an additional malicious query to the original query?


- **Piggybacked query**
- Tautology
- In-line comment
- UNION SQL injection

>Explanation:

> Attackers simplify an SQL injection attack by integrating multiple vulnerable inputs into a single query using in-line comments.
    
> In a **Piggybacked SQL injection attack**, an attacker injects an additional malicious query to the original query. The original query remains unmodified, and the attacker’s query is piggybacked on the original query.
    
> For example, the original SQL query is as given below.

> SELECT * FROM EMP WHERE EMP.EID = 1001 AND EMP.ENAME = 'Bob'

> Now, the attacker concatenates the delimiter (;) and malicious query to the original query as given below.

> SELECT * FROM EMP WHERE EMP.EID = 1001 AND EMP.ENAME = 'Bob';

> DROP TABLE DEPT;

> After executing the first query and returning the resultant database rows, the DBMS recognizes the delimiter and executes the injected malicious query. Consequently, the DBMS drops the table DEPT from the database.
   
> In a **tautology-based SQL injection** attack, an attacker uses a conditional OR clause in such a way that the condition of the WHERE clause will always be true.
   
> In a **UNION SQL injection**, an attacker uses a UNION clause to append a malicious query to the requested query.



### In one of the following methods, an attacker attempts to replicate error-free navigation by injecting simple inputs such as ' and '1' = '1 Or ' and '1' = '2 and forces an application to generate application errors that reveal information such as table names, column names, and data types. Which is this method?


- Type mismatch
- Determining the database engine type
- Parameter tampering
- **Determining a SELECT query structure**

>Explanation:

    
>Determining a SELECT Query Structure: Using which, attackers try to replicate an error free navigation by the injection of simple input such as ' and '1' = '1 Or' and '1' = '2 . To obtain the original query structure, the attacker forces the application to generate application errors that reveal information such as table names, column names, and data types.
    
>Determining Database Engine Type: Determining the database engine type is fundamental to proceeding with the injection attack. ODBC error messages reveal the type of database engine used or enable an attacker to guess and determine which type of database engine might have been used in the application.
    
>Parameter Tampering: An attacker can tamper with HTTP GET and POST requests to generate errors. The Burp Suite or Tamper Chrome utilities can manipulate GET and POST requests.
    
>Type Mismatch: Attackers try to insert strings into numeric fields; the error messages will show the data that could not get converted.



### Which of the following issues can be detected when testers send long strings of junk data, similar to strings for detecting buffer overruns that throw SQL errors on a page?


- SQL injection
- Input sanitization
- **Truncation**
- SQL modification

> Explanation:

    
> Detecting Input Sanitization: testers use right square bracket (the ] character) as the input data to identify instances where the user input is used as a part of an SQL identifier without any input sanitization.
    
> Detecting SQL Modification: Testers send long strings of single quote characters (or right square brackets or double quotes). These max out the return values from REPLACE and QUOTENAME functions and might truncate the command variable used to hold the SQL statement.
    
> Detecting SQL Injection Issues: Testers send single quotes as input data to identify instances where the user input is not sanitized. Send double quotes as input data to identify instances where the user input is not sanitized.
    
> Detecting Truncation Issues: Testers send long strings of junk data, similar to strings to detect buffer overruns; this action might throw SQL errors on the page.


### In which of the following techniques does an attacker use logical requests such as AND/OR to bypass a firewall?


- HPF technique
- **Blind SQL injection**
- CRLF technique
- Normalization method

> Explanation:

    
> CRLF Technique: Carriage return, line feed (CRLF) is a pair of ASCII codes, 13 and 10. In Windows, CRLF is used to indicate the end of a line in a text file (\r\n). Macintosh uses CR (\r) alone and UNIX uses LF(\n) alone.
    
> HPF Technique: HPF is used along with HPP using the UNION operator to bypass firewalls.
    
> Normalization Method: Systematic representation of the database in the normalization process sometimes leads to an SQL injection attack.
    
> Blind SQL Injection: This technique is used to replace WAF signatures with their synonyms using SQL functions. Attackers use logical requests such as AND/OR to bypass the firewall.





### Which of the following queries is used to create a database account in Microsoft SQL Server?


- CREATE USER victor IDENTIFIED BY 'Pass123'
- CREATE USER victor IDENTIFIED BY Pass123 TEMPORARY TABLESPACE temp DEFAULT TABLESPACE users; GRANT CONNECT TO victor; GRANT RESOURCE TO victor;
- INSERT INTO mysql.user (user, host, password) VALUES ('victor', 'localhost', PASSWORD('Pass123'))
- **exec sp_addlogin 'victor', 'Pass123' exec sp_addsrvrolemember 'victor', 'sysadmin'**

> Explanation:

> The following are different ways of creating database accounts in various DBMS:

> Oracle

`CREATE USER victor IDENTIFIED BY Pass123`

`TEMPORARY TABLESPACE temp`

`DEFAULT TABLESPACE users;`

`GRANT CONNECT TO victor;`

`GRANT RESOURCE TO victor;`

> Microsoft Access

`CREATE USER victor`

`IDENTIFIED BY 'Pass123'`

> MySQL

`INSERT INTO mysql.user (user, host, password) VALUES ('victor', 'localhost', PASSWORD('Pass123'))`

> Microsoft SQL Server

`exec sp_addlogin 'victor', 'Pass123'`

`exec sp_addsrvrolemember 'victor', 'sysadmin'`





### Which of the following MSSQL queries allows an attacker to perform column enumeration on a target database?


- SELECT attnum,attname from pg_class, pg_attribute WHERE relname= 'tablename' AND pg_class.oid=attrelid AND attnum > 0
- SELECT * FROM syscat.columns WHERE tabname= 'tablename'
- **SELECT name FROM syscolumns WHERE id = (SELECT id FROM sysobjects WHERE name = 'tablename')**
- SELECT * FROM all_tab_columns WHERE table_name='tablename'

> Explanation:

Column Enumeration in DB

> MSSQL

`SELECT name FROM syscolumns WHERE id = (SELECT id FROM sysobjects WHERE name = 'tablename')`

> Oracle

`SELECT * FROM all_tab_columns WHERE table_name='tablename'`

> DB2

`SELECT * FROM syscat.columns WHERE tabname= 'tablename'`

> PostgreSQL

`SELECT attnum,attname from pg_class, pg_attribute WHERE relname= 'tablename' AND pg_class.oid=attrelid AND attnum > 0`





### William has been hired by the ITSec, Inc. to perform web application security testing. He was asked to perform black box penetration testing to test the security of the company’s web applications. No information is provided to William about the company’s network and infrastructure. William notices that the company website is dynamic and must make use of a backend database. He wants to see if an SQL injection would be possible. As part of the testing, he tries to catch instances where the user input is used as part of an SQL identifier without any input sanitization. Which of the following characters should William use as the input data to catch the above instances?


- **Single quote**
- **Double quote**
- Semicolon
- Right square bracket

> Explanation:

    
> **Single and double quotes**: In black box penetration testing, single and double quotes are used as the input data to catch instances where the user input is not sanitized.
    
> **Semicolon**: In black box penetration testing, a semicolon is used to group two or more SQL statements in the same line.





### In which of the following evasion techniques does an attacker use a WHERE statement that is always evaluated as “true” so that any mathematical or string comparison can be used, such as “' or '1'='1'”?


- Null byte
- Case variation
- **Variations**
- Declare variables

Explanation:

>Variations: Uses the WHERE statement that always evaluates to 'true,' so that any mathematical or string comparison can be used. It is performed by placing characters such as “' or '1'='1'” on any basic injection statement such as“or 1=1” or with other accepted SQL comments.
    
>Declare Variables: Uses variables that can be used to pass a series of specially crafted SQL statements and bypass the detection mechanism.
    
>Case Variation: Obfuscate an SQL statement by mixing it with uppercase and lowercase letters.
    
>Null Byte: Uses the null byte (%00) character prior to a string in order to bypass the detection mechanism.




### Which of the following characters is used in an SQL injection query as a wildcard attribute indicator?


- \#
- ' or "
- /*…*/
- **%**

> Explanation:

The various SQL injection characters are as follows:
1. ' or " character string indicators
2. §-- or # single-line comment
3. /*…*/ multiple-line comment
4. \+ addition, concatenate (or space in URL)
5. || (double pipe) concatenate
6. % wildcard attribute indicator
7. ?Param1=foo&Param2=bar URL Parameters
8. PRINT useful as non-transactional command
9. @variable local variable
10. @@variable global variable
11. waitfor delay '0:0:10' time delay



### In one of the following defensive techniques, only the list of entities such as data type, range, size, and value that have been approved for secured access are accepted. Which is this technique?


- Blacklist validation
- Enforcing least privileges
- Output encoding
- **Whitelist validation**

>Explanation:

> **Output Encoding**: Output encoding is used to encode the input to ensure it is properly sanitized before being passed to the 

> **Whitelist Validation**: Whitelist validation is a best practice whereby only the list of entities (i.e., data type, range, size, value, etc.) that have been approved for secured access is accepted. Whitelist validation can also be termed as positive validation or inclusion.
    
>**Enforcing Least Privileges**: Minimum privileges should be assigned to the operating system where the database management system runs, and the DBMS should never be run as root.
    
>**Blacklist Validation**: Blacklist validation rejects all the malicious inputs that have been disapproved for protected access.



### Which of the following is a Snort rule that is used to detect and block an SQL injection attack?


- SqlDataAdapter myCommand = new SqlDataAdapter("LoginStoredProcedure '" + Login.Text +"'", conn);
- UNION Select Password
- **/(\%27)|(\')|(\-\-)|(\%23)|(#)/ix**
- ' OR 5 BETWEEN 1 AND 7

> Explanation:

> Many of the common attacks use specific type of code sequences or commands that allow attackers to gain an unauthorized access to the target's system and data. These commands and code sequences allow a user to write Snort rules that aim to detect SQL injection attacks.

> Some of the expressions that can be blocked by the Snort are as follows:

> /(\%27)|(\')|(\-\-)|(\%23)|(#)/ix

> /exec(\s|\+)+(s|x)p\w+/ix

> /((\%27)|(\'))union/ix

> /\w*((\%27)|(\'))((\%6F)|o|(\%4F))((\%72)|r|(\%52))/ix

> alert tcp $EXTERNAL_NET any -> $HTTP_SERVERS $HTTP_PORTS (msg:"SQL Injection - Paranoid"; flow:to_server,established;uricontent:".pl";pcre:"/(\%27)|(\')|(\-\-)|(%23)|(#)/i"; classtype:Web-application-attack; sid:9099; rev:5




### Finch, a security professional, was tasked with securing an organization's database from SQL injection attacks. For this purpose, he updated the code using the Replace () method and inserted wildcard characters such as % and [ between the square brackets so that such characters are omitted from the actual code.

Identify the defensive technique employed by Finch in the above scenario.


- Whitelist validation
- Wrapping parameters with QUOTENAME () and REPLACE ()
- Enforcing least privileges
- **LIKE clauses**

> Explanation:
    
> **Whitelist Validation**: Whitelist validation is a best practice whereby only the list of entities (i.e., data type, range, size, value, etc.) that have been approved for secured access is accepted.
    
> **LIKE Clauses**: While using a LIKE clause, wildcard characters such as _, %, and [ should be escaped. For that purpose, use the Replace() method and insert these wildcards between square brackets, which can protect the code from SQL injection.
    
> **Enforcing Least Privileges**: Enforcing least privileges is a security best practice whereby the lowest level of privileges is assigned to every account accessing the database.
    
> **Wrapping Parameters with QUOTENAME()and REPLACE()**: The data received from the parameters used in the stored procedure or the data received from the existing tables should be wrapped using QUOTENAME() and REPLACE().

