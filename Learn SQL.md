# Learn SQL 

[Website Reference](https://https://www.sql-practice.com/)

[TOC]

## Database 'Hospital'
### Easy
- Show first name, last name, and gender of patients whose gender is 'M'

```sql_more=
SELECT first_name, last_name, gender 
FROM patients 
WHERE gender = 'M';
```

- Show first name and last name of patients who does not have allergies. (null)

```sql_more=
SELECT first_name, last_name
FROM patients
WHERE allergies is null;
```
- Show first name of patients that start with the letter 'C'

```sql_more=
SELECT first_name
FROM patients
WHERE first_name LIKE 'C%';
```

```sql_more=
-- other solution
SELECT first_name
FROM patients
WHERE substring(first_name, 1, 1) = 'C';
```

- Show first name and last name of patients that weight within the range of 100 to 120 (inclusive)

```sql_more=
SELECT first_name, last_name
FROM patients
WHERE weight between 100 and 120;
```

```sql_more=
-- other solution
SELECT
  first_name,
  last_name
FROM patients
WHERE weight >= 100 AND weight <= 120;
```

- Update the patients table for the allergies column. If the patient's allergies is null then replace it with 'NKA' (no known allergies)
```sql_more=
UPDATE patients
SET allergies = 'NKA'
WHERE allergies is null;

--- display the patients table to check results
SELECT * FROM patients;
```

### Medium


### Hard