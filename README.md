🎯 Overview
A hands-on lab demonstrating Dynamic Data Masking (DDM) in SQL Server. The project walks through creating a sample table with sensitive user data, applying different masking techniques, and testing how masked data appears to a restricted user versus a privileged one.

🔒 What is Data Masking
Data masking deals with techniques used to protect sensitive information while keeping data useful for analysis, sharing, or testing, without risking exposure of the real values.

💡 Purpose
The primary goal is to protect sensitive data from unauthorized access, while still providing a functional alternative for scenarios where the real data is not necessary.

🛠 Environment
Database: SQL Server.
Table: UserData, containing CustomID, FirstName, LastName, Email, DateOfBirth, and CreditCardNumber.

📋 Steps Covered

1. Create the table and insert sample data.
2. Apply default masking on the FirstName column.
3. Create a restricted user, TESTUSER, without server login access.
4. Grant TESTUSER SELECT permission on the dbo schema.
5. Switch execution context to TESTUSER and confirm masking is applied.
6. Apply partial masking on CreditCardNumber, showing only the last four digits.
7. Apply partial masking showing only the first four digits.
8. Apply full masking, replacing the entire value with x's.
9. Apply email masking using the built in email() function.
10. Remove masking from a column using DROP MASKED.
11. Grant the UNMASK permission to TESTUSER to reveal original data.

✅ Key Takeaways
Dynamic Data Masking limits exposure of sensitive columns without changing the underlying data.
Masking rules apply based on user permissions, not on the data itself.
The UNMASK permission fully overrides masking for a given user, so it should be granted carefully.
This technique is useful for development, testing, and reporting environments where full data access is not required.

⚠️ Disclaimer
All data used in this lab is sample or fictitious. This project was built for educational purposes to demonstrate SQL Server security features.

📄 License
This project is licensed under the MIT License.

