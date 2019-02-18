# minggu-10


Build a Python App database with CockroachDB
1.	Download and extract the CockroachDB v2.1.1 archive for Windows
o	cockroach.exe version -> melihat versi dari CockroachDB
o	start cockroach.exe -> menjalankan CockroachDB

masuk ke Start a Local Cluster Insecure
1.	cockroach start --insecure --listen-addr=localhost
o	In a new terminal, add the second node:
•	   --insecure \
•	   --store=node2 \
•	   --listen-addr=localhost:26258 \
•	   --http-addr=localhost:8081 \
•	   --join=localhost:26257
o	In a new terminal, add the third node:
•	   --insecure \
•	   --store=node3 \
•	   --listen-addr=localhost:26259 \
•	   --http-addr=localhost:8082 \
•	   --join=localhost:26257
2.	Test the cluster -> membuat database

Build a Python App with CockroachDB
1.	Install the psycopg2 driver
2.	Run the Python code
o	buat configurasi dengan nama basic-sample.py
o	jalankan basic-sample.py

o	buat configurasi dengan nama txn-sample.py
o	jalankan txn-sample.py
o	To verify that funds were transferred from one account to another, start the built-in SQL client
o	To check the account balances, issue the following statement:

