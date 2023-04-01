---
title: SQL Transaction
tags: computer-science sql
---

# SQL Transaction

In [[sql|SQL]], a **transaction** bundles multiple steps into a single operation that is performed against a database.

Transactions must be controlled to ensure the integrity of the database.

There are four standard properties to transactions:

1. **Atomicity** - ensure all operations are completed successfully
2. **Consistency** - ensure database properly changes state upon successfully committed transactions
3. **Isolation** - enables transactions to operate independently from one another
4. **Durability** - ensure that effects of a transaction persist even after database or system failure

## Sources

- <https://www.postgresql.org/docs/current/tutorial-transactions.html>
- <https://www.tutorialspoint.com/sql/sql-transactions.htm> 
