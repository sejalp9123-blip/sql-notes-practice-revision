
# SQL String Functions

SQL string functions help manipulate and format text data. They are used for cleaning, comparing and extracting meaningful information from textual fields.

## 📌 Categories of String Functions

We can categorize String functions into 3 categories:

1. **String Manipulation**
   - `CONCAT()`
   - `UPPER()`
   - `LOWER()`
   - `TRIM()`
   - `REPLACE()`

2. **String Calculation**
   - `LEN()`

3. **String Extraction**
   - `LEFT()`
   - `RIGHT()`
   - `SUBSTRING()`


---

## 1] Concat()

It is used to combine multiple strings into single string

**Syntax:**

```sql
CONCAT(String1, String 2,.....)
````

**For Ex:**

```sql
Select CONCAT('JOE', ' ', 'Richey') as FullName;
```

**Output:**

```text
JOE Richey
```

---

## 2] UPPER()

It converts all the characters of string into uppercase.

**Syntax:**

```sql
UPPER(String)
```

**For Ex**

```sql
Select UPPER('Martin') as Upper_name;
```

**Output:**

```text
MARTIN
```

---

## 3] LOWER()

It converts all the characters of String into Lowercase.

**Syntax:**

```sql
LOWER(string)
```

**For Ex**

```sql
Select LOWER('MARTIN') as lower_name;
```

**Output:**

```text
martin
```

---

## 4] TRIM():

It removes the leading and trailing spaces from the String

**Syntax:**

```sql
TRIM([BOTH | LEADING | TRAILING] [remstr] FROM string)
```

### Components of the Syntax:

* **BOTH (Default):** Removes the specified characters from the front and back.
* **LEADING:** Removes the specified characters only from the front (left side).
* **TRAILING:** Removes the specified characters only from the back (right side).
* **remstr:** The specific characters you want to delete (default is the empty String).
* **string:** The target text you want to clean up.

### Examples:

#### 1] Standard Trim (Removes the spaces from both ends)

If you do not specify any parameters then by default it strips spaces from both the ends.

**For Ex**

```sql
select TRIM('  Hello World  ') as Result;
```

**Output:**

```text
Hello World
```

#### 2] Remove Leading characters

Removes specified characters/numbers only from the beginning of the string.

**For Ex**

```sql
Select TRIM(LEADING '0' FROM '000092675431') as Result
```

**Output:**

```text
92675431
```

#### 3] Remove trailing characters

Removes specified characters/numbers only from the end of the string.

**For Ex**

```sql
Select TRIM(TRAILING '-' FROM 'Hello World---') as Result
```

**Output:**

```text
Hello World
```

#### 4] Remove specific characters from both the ends.

Removes specified characters from both th ends.

**For Ex**

```sql
Select TRIM(BOTH '#' FROM '###7853580##') as Result
```

**Output:**

```text
7853580
```

---

## 5] REPLACE():

It is used to replace all the occurences of substring/character within a given string, with a new substring.

**For Ex**

```sql
REPLACE(String, Old_Substring, New_Substring)
```

### Components of the Syntax:

* **String:** The original string
* **Old_Substring:** The Substring to be replaced
* **New_Substring:** The new replacement Substring

**For Ex:**

```sql
Select REPLACE('Welcome to the Snowflake Tutorial', 'Snowflake', 'SQL') as new_string;
```

**Output:**

```text
Welcome to the SQL Tutorial
```

---

## LEN()

Len() is the function used to calculate the size of a string.

Note: In most database engines like PostgreSQL, Oracle, and SQLite, the function is named LENGTH(). In Microsoft SQL Server (T-SQL), it is named LEN().

**Syntax:**

```sql
Len(String)
```

**For Ex:**

```sql
Select len('Hello') as length;
```

**Output:**

```text
5
```

---

# LEFT(), RIGHT(), and SUBSTRING()

LEFT(), RIGHT(), and SUBSTRING() are functions used to extract specific parts of string.

## 1] LEFT:

Extracts the specified number of characters starting from the beginning (left side) of a string.

**Syntax:**

```sql
LEFT(string, number)
```

**For Ex:**

```sql
Select LEFT('Hello World', 5) as string1;
```

**Output:**

```text
Hello
```

---

## 2] RIGHT():

Extracts the specified number of characters starting from the end (right side) of a string.

**Syntax:**

```sql
RIGHT(string, number)
```

**For Ex:**

```sql
Select RIGHT('Hello World', 5) as string1;
```

**Output:**

```text
World
```

---

## 3] SUBSTRING():

Extracts the part of string at specific position and length.

**Syntax:**

```sql
SUNSTRING(String, Start_Position, Length)
```

**Note:** In SQL, string indexing is 1-based (the first character is at position 1, not 0)

**For Ex:**

```sql
Select SUBSTRING('Hello World', 7, 3) as string1;
```

**Output:**

```text
Wor
```









