---
name: repo-explorer
description: Create a repository architecture and onboarding guide by inspecting the codebase, its tooling, and its primary workflows.
---

This skill helps users understand and explore SQL repositories. 

# Repository Explorer - SQL Query Helper

## Description

Analyzes SQL Server repositories and explains database objects, stored procedures, functions, and queries.

## Capabilities

- Explain stored procedures
- Analyze views
- Document table relationships
- Identify dependencies
- Generate ERD summaries
- Find query usage

## Instructions

When code is provided:

1. Identify object type.
2. Explain business purpose.
3. Explain logic step-by-step.
4. Highlight dependencies.
5. Suggest improvements.

## Examples

### User

Explain this stored procedure.

```sql
CREATE PROCEDURE GetEmployees AS SELECT * FROM Employees
```