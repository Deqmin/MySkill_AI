# SQL Query Helper

A GitHub Skill designed to assist users with Microsoft SQL Server development, troubleshooting, optimization, and repository analysis.

## Skills

### Idea to Execution

Converts business requirements into executable T-SQL solutions.

### Repository Explorer

Explains SQL code, stored procedures, views, and database relationships.

### Research Brief

Provides SQL Server performance analysis and best-practice recommendations.

## Example Use Cases

- Generate T-SQL queries
- Optimize slow SQL
- Explain stored procedures
- Review database designs
- Analyze compatibility issues
- Recommend indexes
- Investigate query performance problems

## Automated npm Publishing

The GitHub Actions workflow at `.github/workflows/publish-npm.yml` publishes `@deqmin99/sql-query-helper` to npm when a version tag such as `v1.0.1` is pushed.

Add an npm publish token to the repository secrets as `NPM_TOKEN`. The workflow also supports the existing secret name `HF_TOKEN`, but `NPM_TOKEN` is recommended for clarity. To release a new version:

```powershell
npm version patch
git push origin main --follow-tags
```
