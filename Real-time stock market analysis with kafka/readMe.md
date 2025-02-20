# Stock Market Real-Time Data Analysis Using Kafka

In this project, I develop an End-To-End Data Engineering Project on Real-Time Stock Market Data using Kafka.

I'll use different technologies such as Python, Amazon Web Services (AWS), Apache Kafka, Glue, Athena, and SQL.

This is the project architecture

![Architecture](https://github.com/user-attachments/assets/b3cd878c-a907-4fab-9c4f-d69a1a2f57e7)

# Data flow


Zookeeper(left) and kafka(right)
![{BD62E042-DE1F-4B8E-8FEE-E6C68F9BC077}](https://github.com/user-attachments/assets/5b754768-08cb-48b6-a285-75c26f63be2f)

Updating security groups
![{A7949245-E571-4C9F-BE30-58BC107EB810}](https://github.com/user-attachments/assets/23f37768-09bc-46de-9722-c7374edd7fa7)

Produces(left) and consumer(right)

![{DCD09FED-3662-4C9C-A8B5-C4B35A9C89AD}](https://github.com/user-attachments/assets/9e625501-eca5-4803-9f47-c0a4cd595448)

Using the producer | Check the dataset

![{2B901962-7C53-4B2C-B4B8-6998DBB924CC}](https://github.com/user-attachments/assets/d9a49728-41ec-4a64-9c47-49d8610d8d21)

Sending massive data from de producer

![{5B412503-AA95-4895-81CA-172B8E0417CA}](https://github.com/user-attachments/assets/93a756f7-b8fe-49e7-8650-2b7ec85135b1)

Receiving the data(It broke the server since it was only a t2-micro)

![{1D6108C4-F6F2-4B21-A947-6E359BCB6AFA}](https://github.com/user-attachments/assets/49f00f52-3452-4abf-9ed7-f50ce301e2bc)

Taking the information and saving it in the bucket
![{69913B3A-A2E2-493D-ABFE-BDF484C72F52}](https://github.com/user-attachments/assets/47d957e4-3400-4f21-8b4e-ba9505ce1eff)

![{7B890FFA-4987-4271-AC0A-4CBB588C8BDB}](https://github.com/user-attachments/assets/7f4c1582-f738-4a7d-81da-580153d5f3ac)

A crawler was created to make the data available for querying from athena

![{5D9FA31B-B407-41E5-9E67-B601ED1496D5}](https://github.com/user-attachments/assets/85e107c1-0fc8-4e2e-a3d1-742c2ef0a7cb)

This is how the table look in athena

![{E71B83F9-3CA2-4496-9EA9-DA8ED5F1B2F2}](https://github.com/user-attachments/assets/315a516a-9faf-46fa-8418-c8e5693a5b3f)

# Final Comments

This was a project where I didn't learned much about aws since I used tools that I'm already used to but I learned a lot about kafka and zookeper. I had some problems with the RAM in the machine since it was only 1MB but adjusting some parameters from the JVM it fixed.  
