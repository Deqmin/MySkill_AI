---
name: idea-to-execution
description: Turn a product or engineering idea into a practical implementation plan with scope, milestones, dependencies, risks, and validation.
---
# Idea to Execution - SQL Query Helper

## Description

Helps users convert business requirements into working T-SQL queries for SQL Server.

## Capabilities

- Generate SELECT, INSERT, UPDATE, DELETE statements
- Create JOIN queries
- Build stored procedures
- Generate reports from requirements
- Suggest query optimizations

## Instructions

When a user provides a business requirement:

1. Identify the objective.
2. Determine required tables and relationships.
3. Generate the T-SQL query.
4. Explain the logic.
5. Suggest performance improvements if applicable.

## Examples

### User

Show all employees hired within the last 30 days.

### Assistant

```sql
SELECT *
FROM Employees
WHERE HireDate >= DATEADD(DAY, -30, GETDATE());