# 🚀 How to Save SQL Commands & Output to Notepad in SQL*Plus

This guide will help you **log all SQL commands and their outputs** into a Notepad file for later use. ✅

---

## 📌 Step 1: Open Command Prompt & Get Database Name

🔹 First, open **Command Prompt (cmd)** and retrieve your **database name** using SQL*Plus:

```sql
SELECT * FROM GLOBAL_NAME;
```
✅ **Example Output:**  
```
ORCL.RDBMS.DEV.US.ORACLE.COM
```

---

## 📌 Step 2: Connect to SQL*Plus

🔹 Run the following command to start SQL*Plus **from cmd**:

```cmd
sqlplus username/password@dbname
```
✅ Example:
```cmd
sqlplus SCOTT/tiger@ORCL.RDBMS.DEV.US.ORACLE.COM
```
- Now, you're **inside SQL*Plus (`SQL>`)**.

---

## 📌 Step 3: Enable Command Logging Using `SPOOL`

🔹 SQL*Plus does **not track history** by default, but you can **log everything** using the `SPOOL` command:

```sql
SPOOL sql_history.log;
```
✅ **What this does?**
- It starts saving **all commands & outputs** into the file `sql_history.log`.

---

## 📌 Step 4: Run Your SQL Commands

🔹 Execute your required SQL queries. **Example:**

```sql
SELECT * FROM EMP;
```
Everything will be saved in **`sql_history.log`**. 📜

---

## 📌 Step 5: Stop Logging & Save the File

🔹 Once you're done, **stop logging** with:

```sql
SPOOL OFF;
```
✅ **Now, all executed commands & their outputs** are saved inside `sql_history.log`.

---

## 📌 Step 6: Open the Log File in Notepad

🔹 Open a **new Command Prompt tab** and run:

```cmd
notepad sql_history.log
```
✅ **This will open the file with**:
- All executed SQL commands
- Their corresponding outputs

🎉 **Now enjoy your SQL history inside Notepad!** 🎉

---


---

## 🔹 Summary of Commands

| 🔢 Step | Command | Purpose |
|---------|---------|---------|
| **1️⃣** | `SELECT * FROM GLOBAL_NAME;` | Get database name |
| **2️⃣** | `sqlplus username/password@dbname` | Connect to SQL*Plus |
| **3️⃣** | `SPOOL sql_history.log;` | Start logging |
| **4️⃣** | `SELECT * FROM EMP;` | Run SQL queries |
| **5️⃣** | `SPOOL OFF;` | Stop logging |
| **6️⃣** | `notepad sql_history.log` | Open log file |

---


