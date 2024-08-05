# SQL Queries

Following links contains database dumps and all SQL queries. Click to be redirected and download:

- [Characters Dump](https://drive.google.com/file/d/1aouJWJEOBXxIfR5RNekctdIimpgfzjo7/view?usp=sharing)
- [Library Dump](https://drive.google.com/file/d/1hsHqN83engEs6HhtCEn2Ka3tQPk0e6ht/view?usp=sharing)



## Write the first and last name of the characters whose last name is Crabbe, Granger or Diggory

**Description:**
This query retrieves the first and last names of characters whose last name is Crabbe, Granger, or Diggory.

**SQL Query:**

```sql
SELECT fname, lname
FROM characters
WHERE lname IN ('Crabbe', 'Granger', 'Diggory')
  ```

**Result Example**

| fname    | lname   |
|----------|---------|
| Hermione | Granger |
| Vincent  | Crabbe  |
| Cedric   | Diggory |

------------------------------------------------------------------------------------------

## Print the id and names of all patronuses in alphabetical order, provided they are known.

**Description:**
This query prints the IDs and names of all known Patronuses in alphabetical order.

**SQL Query:**

```sql
SELECT char_id, patronus
FROM characters
WHERE NOT patronus = 'Unknown' AND patronus IS NOT NULL
ORDER BY patronus ASC
  ```

**Result Example**

| char_id | patronus             |
|---------|----------------------|
|      10 | Doe                  |
|       8 | Hare                 |
|       3 | Jack Russell terrier |
|       2 | Otter                |
|       7 | Phoenix              |
|       1 | Stag                 |

------------------------------------------------------------------------------------------

## Calculate the number of characters per faculty, leaving only those faculties where the number of students is greater than 1.

**Description:**
This query calculates the number of characters per faculty and includes only those faculties where the number of students is greater than 1.

**SQL Query:**

```sql
SELECT count(char_id), faculty
FROM characters
GROUP BY faculty
HAVING count(char_id) > 1
  ```

**Result Example**

| count(char_id) | faculty    |
|----------------|------------|
|              4 | Gryffindor |
|              5 | Slytherin  |

------------------------------------------------------------------------------------------

## Write the first and last name of the characters and the name of the book that belongs to them.

**Description:**
This query retrieves the first and last names of the characters along with the name of the book that belongs to them.

**SQL Query:**

```sql
SELECT characters.char_id, characters.fname, characters.lname, library.book_name
FROM characters
LEFT JOIN library on characters.char_id = library.char_id
WHERE characters.char_id IS NOT NULL
  ```

**Result Example**

| char_id | fname    | lname      | book_name                                  |
|---------|----------|------------|--------------------------------------------|
|       1 | Harry    | Potter     | Magical Water Plants Of The Highland Rocks |
|       2 | Hermione | Granger    | A History Of Magic                         |
|       3 | Ron      | Weasley    | Advanced Potion-Making                     |
|       4 | Draco    | Malfoy     | Fantastic Beasts And Where To Find Them    |
|       ... | ...  | ...     | ...    |

------------------------------------------------------------------------------------------

## Print the names of all patronus whose owners are older than the character whose patronus is Unknown.

**Description:**
This query prints the names of all Patronuses whose owners are older than the character whose Patronus is "Unknown".

**SQL Query:**

```sql
SELECT fname
FROM characters
WHERE age > (
        SELECT age
        FROM characters
        WHERE patronus = 'Unknown'
)

  ```

**Result Example**

| fname   |
|---------|
| Albus   |
| Severus |

