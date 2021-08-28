##### Big_Data_GCP_dataproc_spark_hadoop
# Big Data GCP dataproc spark hadoop


<!-- <p align="center"><img src="./DIO.png" width="500"></p> -->

### Goal

The goal of this project is to __*Create a fully managed Hadoop Big Data Ecosystem with Dataproc on Google Cloud Platform - GCP*__. This product aims to test the knowledge acquired in Bootcamp Data Engineer. A partnership between Banco Carrefour and Digital Innovation One.

The challenge is to perform data processing using the Dataproc product from GCP. This processing will count the words of a book in .TXT format and inform how many times each word contained in the book appears.

---

### Phases

NOTE: For security reasons the bucket name has been omitted.

1. Create a bucket on Cloud Storage
1. Update the ```counter.py``` file with the name of the Bucket created in the lines that contain ```{NAME_OF_YOUR_BUCKET}```.
1. Upload the ```counter.py``` and ```book.txt``` files to the bucket you created (instructions below)
     - https://cloud.google.com/storage/docs/uploading-objects
1. Use the code in a Dataproc cluster, running a PySpark-type Job by calling ```gs://{NAME_OF_YOUR_BUCKET}/counter.py```
1. The Job will generate a folder in the bucket called ```result```. Inside that folder the ```part-00000``` file will contain the list of words and how many times it is repeated throughout the book.

---

### Delivery of Results

1. Create a repository on your GitHub.
2. Create a file called ```result.txt```. Inside this file, put the 10 words that are most used in the book, according to the Job result.
3. Insert the ```result.txt``` and ```part-00000``` files into the repository
4. Inform the repository link on the Digital Innovation One platform in the "DELIVER PROJECT" session

---

### Tips

-> If the Job shows an "Interrupt WARN", just ignore it. There is a known bug in Hadoop. This does not impact processing.

-> to open files for editing use the command:

     vim + file_name.extension

-> to save file in GCP Shell:

     type colon + wq! + ENTER
     like this :wq!ENTER

-> how to open just to view:
  
     cat + filename.extension
