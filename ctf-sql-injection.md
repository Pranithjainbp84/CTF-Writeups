🕵️ Incident:

The challenge required exploiting an SQL injection vulnerability in a vulnerable web application. The objective was to retrieve sensitive data from the backend database.

🔎 Investigation:

- Step 1: Identified a vulnerable login form where user input was not sanitized.
- Step 2: Used SQL injection techniques such as ' OR 1=1 -- to bypass authentication and access the system.
- Step 3: Once inside, performed a series of UNION SELECT statements to enumerate tables and columns in the database.
- Step 4: Retrieved usernames, passwords (hashed), and other sensitive data from the database.

🛡️ Mitigation:

- Step 1: Recommended implementing prepared statements and parameterized queries to avoid SQL injection vulnerabilities.
- Step 2: Suggested applying input sanitization on all user inputs and using ORM frameworks to prevent raw SQL queries.
- Step 3: Set up Web Application Firewalls (WAF) to monitor and block SQL injection patterns in web traffic.
