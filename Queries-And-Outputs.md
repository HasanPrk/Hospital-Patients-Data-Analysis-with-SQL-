```sql
-- Question 1 --

SELECT
    First_name AS 'First Name',
    Last_name AS 'Last Name',
    Gender AS 'Gender'
FROM Patients
WHERE Gender = 'M'
ORDER BY Last_name, First_name;
GO
```
<img width="407" height="406" alt="image" src="https://github.com/user-attachments/assets/4a5e6c67-fdee-4ccc-9b18-894cd7cfc006" />

```sql
-- Question 2 --
SELECT
	First_name AS 'First Name',
	Last_Name AS 'Last Name'
FROM patients
WHERE allergies is Null
ORDER BY last_name, first_name;
GO
```
<img width="397" height="422" alt="image" src="https://github.com/user-attachments/assets/d7e3c34d-c8de-43e6-8cbe-cb5a3d946b60" />

```sql
-- Question 3 --
SELECT
	First_name AS 'First Name'
FROM patients
WHERE first_name LIKE 'C%'
GO
```
<img width="284" height="415" alt="image" src="https://github.com/user-attachments/assets/405e61eb-b59a-4601-862f-5f6c5bf1fd6a" />

```sql
-- Question 4 --
SELECT 
	first_name AS 'First Name',
	last_name AS 'Last Name',
	gender As 'Gender',
	birth_date AS 'Birth-Date',
	city AS 'City',
	ISNULL(allergies, 'NKA') AS 'Allergies',
	height AS 'Height',
	weight AS 'Weight'
FROM patients
GO
```
<img width="940" height="315" alt="image" src="https://github.com/user-attachments/assets/e9f1421c-8a25-4868-b16d-d22ae9d5f39e" />

```sql
-- Question 5 --
SELECT 
	first_name AS 'First Name',
	last_name AS 'Last Name'
FROM patients
WHERE weight BETWEEN 100 AND 120
GO
```
<img width="315" height="419" alt="image" src="https://github.com/user-attachments/assets/3e007936-834d-4485-b161-2a4648f5c3d1" />

```sql
-- Question 6 --
SELECT 
	CONCAT(first_name,' ', last_name) AS 'Full Name'
FROM patients
GO
```
<img width="261" height="417" alt="image" src="https://github.com/user-attachments/assets/731bce36-f98b-4013-8989-f02ea08799b1" />

```sql
-- Question 7 --
SELECT 
	COUNT(*) AS 'Number of Patients Born in 2010'
FROM patients
WHERE YEAR(birth_date) = '2010'
GO
```
<img width="336" height="131" alt="image" src="https://github.com/user-attachments/assets/8aa225d7-30f3-4502-b4b2-c97adaffb637" />

```sql
-- Question 8 --
SELECT *
FROM patients
WHERE patient_id in (1,45,534,879,1000)
GO
```
<img width="952" height="192" alt="image" src="https://github.com/user-attachments/assets/da67089f-eb99-4589-ad80-1b3360c28dd6" />

```sql
-- Question 9 --
SELECT 
	first_name AS 'First Name',
	last_name AS 'Last Name',
	birth_date AS 'Birth Date' 
FROM patients
WHERE height > 160 AND weight > 70
GO
```
<img width="421" height="400" alt="image" src="https://github.com/user-attachments/assets/cfaeced3-52c9-4b68-9951-b4f604be7dc3" />
