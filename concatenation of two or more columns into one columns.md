# concatenation of two or more columns into one columns in linux

* Open file path data you want to concate
* Create header and insert data name columns. example: header_transaction.txt

<img width="483" alt="image" src="https://user-images.githubusercontent.com/110078907/184283579-13dc6422-ce43-452f-921b-12f48d23cfdc.png">


view file contents:

    head header_transaction.txt

<img width="491" alt="image" src="https://user-images.githubusercontent.com/110078907/184283839-206e3aa0-64da-4ab4-b8f0-f71c020ba3e8.png">


* insert data name columns to data_transaction.txt

delimiter ',' don't insert 'IGNORE'

<img width="484" alt="image" src="https://user-images.githubusercontent.com/110078907/184283989-3b584793-371d-4fc5-b10e-c95918f22bd7.png">


* example table concate:
tblid=$4, tbltcd=$5, time_pr=$49

command :

      awk -F',' -vOFS=',' '{ $(NF+1)=$4$5$49 ;print}' /home/neo4j/neo4j-enterprise-4.4.9/import/data/202104/dm_transaction/awkconcate/data_transaction.txt > /home/neo4j/neo4j-enterprise-4.4.9/import/data/202104/dm_transaction/awkconcate/data_transaction_concate.txt


<img width="486" alt="image" src="https://user-images.githubusercontent.com/110078907/184285476-91867349-d914-4c8e-8a83-48ab5f49d931.png">


Done! data is concate!

Example: data_transaction_concate.txt

<img width="484" alt="image" src="https://user-images.githubusercontent.com/110078907/184285707-277e334d-16f1-483a-8626-9ff1b0075322.png">


data before :

<img width="488" alt="image" src="https://user-images.githubusercontent.com/110078907/184286039-7c918649-ce17-488c-812d-46d10fa79c5e.png">
