# 💾 GenAI Prompts: SQL & Data Integrity Testing

Strategic prompts to ensure backend reliability, data consistency, and edge case coverage in complex databases.

---

## Prompt 1: Test Data Generation Strategy
> **Role:** Senior Data Quality Engineer.
> **Context:** A relational database with 'Users', 'Orders', and 'Payments' tables.
> **Task:** Create a strategy to generate 100 rows of synthetic test data. 
> **Requirements:** > 1. Ensure referential integrity (Foreign Keys).
> 2. Include edge cases: null values in optional fields, maximum string lengths, and boundary dates.
> 3. Provide the SQL INSERT statements.

## Prompt 2: ACID Compliance & Transaction Testing
> **Task:** Act as a Backend Tester. I am testing a funds transfer feature.
> **Task:** Generate a list of 5 test scenarios to verify ACID properties (Atomicity, Consistency, Isolation, Durability). 
> **Output:** Include the SQL scripts to simulate a "Rollback" when a transaction fails mid-process.

## Prompt 3: Data Migration Validation
> **Context:** We are migrating user profiles from a legacy system (Table A) to a new schema (Table B).
> **Task:** Generate a "Data Mapping" validation script in SQL to compare:
> 1. Row counts between Source and Target.
> 2. Data type mismatches.
> 3. Truncated strings or precision loss in decimal fields.

## Prompt 4: Complex Join & Logic Auditing
> **Task:** Create a SQL query to identify "Orphan Records" (Orders without an associated User) and "Duplicate Transactions" (same User, same Amount, within 60 seconds).
> **Goal:** This query will be used for automated sanity checks in our staging environment.
