# SQL Injection 

## Background
- **SQL (Structured Query Language)**: programming language used to create, interact with, and request information from a database.
- Widely supported across many different database products — makes it one of the most common languages for database interaction.
- **SQL injection**: a type of attack that executes unexpected/malicious queries on a database.
- Used by threat actors to **modify, delete, or steal** information from databases.
- A common attack vector for gaining **unauthorized access** to web applications.
- Regularly listed in the **OWASP® Top 10** — largely because developers tend to focus on making apps *work correctly* rather than securing them against injection.

## SQL Queries
- **Database**: an organized collection of information/data stored in one place (e.g., employee directories, customer payment info).
- In SQL, data is organized into **tables**.
- SQL is used to **retrieve, insert, update, or delete** table data through queries.
- **SQL query**: a request for data from a database (e.g., pulling employee IDs, names, job titles).
- Queries are typically initiated through **input fields** — features that accept text, such as:
  - Login forms
  - Search bars
  - Comment submission boxes
- **Injection occurs** when an attacker exploits an input field that isn't programmed to filter out unwanted/unexpected text.
- Consequences: manipulating databases, stealing sensitive data, or taking control of vulnerable applications.

## 3 Categories of SQL Injection

### 1. In-Band (Classic) Injection
- **Most common type**.
- Uses the **same communication channel** to both launch the attack *and* retrieve the results.
- Example: A retailer's product search box is vulnerable → attacker enters a malicious query → database executes it and returns sensitive data (like passwords) → results display back in that same search box.

### 2. Out-of-Band Injection
- Uses a **different communication channel** to launch the attack vs. to gather results.
- Example: Attacker crafts a malicious query that creates a separate connection between the vulnerable website and a database *they* control — bypassing the website server's built-in security controls to steal data.
- **Note**: Uncommon in practice — only works if specific features are enabled on the target server.

### 3. Inferential Injection
- Attacker **cannot directly see** the results of the attack.
- Instead, they **infer information by observing system behavior** (e.g., error messages, response times).
- Example: An attacker injects a query into a login form that produces an error message. While no data is directly returned, the error reveals clues about the database's structure — which the attacker can use to craft more targeted attacks later.

## Injection Prevention
- SQL queries are often built with the assumption that users will only enter *expected*, well-formatted input (e.g., an email like `jdoe@domain.com`) — but attackers exploit cases where this assumption fails.
- Core defense principle: **escape user inputs** — prevent unexpected code from being inserted and executed.
- Key techniques:
  - **Prepared statements** – a coding technique where SQL statements are executed in a fixed structure *before* user input is passed to the database, separating code from data.
  - **Input sanitization** – programming that strips out or neutralizes input that could be interpreted as executable code.
  - **Input validation** – programming that checks user input matches the system's expected format (length, type, characters, etc.) before processing it.
- Best practice: use a **combination** of these techniques rather than relying on just one.
- Security professionals often need to **collaborate with application developers** to identify and close these gaps.
- Resource: **[OWASP's SQL Injection Detection Techniques](https://owasp.org/www-project-web-security-testing-guide/latest/4-Web_Application_Security_Testing/07-Input_Validation_Testing/05-Testing_for_SQL_Injection)** guide — useful for investigating vulnerabilities firsthand.

## Key Takeaways
- SQL injection is common largely *because* of SQL's widespread use in web applications.
- Like other injection attacks, it stems from **unexpected or unfiltered user input**.
- Defense requires a mix of technical prevention methods (prepared statements, sanitization, validation) and **close collaboration between security teams and developers**.