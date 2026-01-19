# file_int_check
A program that checks integrity of the file 

It detects unauthorized file changes and ensures files are not modified, deleted, or replaced. It uses cryptographic hashes to verify integrity.


How does it works:

1️⃣ Select file(s) to monitor

2️⃣ Generate hash (baseline)

3️⃣ Store hash securely

4️⃣ Re-check file later

5️⃣ Compare new hash with stored hash

6️⃣ If mismatch → alert




