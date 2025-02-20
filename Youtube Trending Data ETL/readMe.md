# Youtube Data Trending Proyect

In this proyect I take information from a popular dataset that gathers information from the youtube API. You cand find the dataset here https://www.kaggle.com/datasets/datasnaek/youtube-new
# Introduction and abstract

This is the project architecture
![architecture](https://github.com/user-attachments/assets/765e579c-e559-4f90-a431-dbdc354f1f88)

# Dataflow

At the start I have the s3 buckets were all information is going to be stored. First, the dataset raw information is uploaded and stored in datae-on-youtube-raw-useast1-dev(last bucket in the picture)
![{1DB2C9F0-782C-4A6C-91DC-57DC822C1DCF}](https://github.com/user-attachments/assets/a872720e-fc47-4c50-ac50-ed95df2d1448)

When this information is uploaded a lambda function is excecuted to convert from JSON to parquet. This new format is stored in the cleansed version bucket.

![{322BC821-E2D1-4A81-A647-85E38E4CA4F7}](https://github.com/user-attachments/assets/132ff6f4-9a77-47f1-96fe-7af68f15585f)

Now, for the csv data, a job is used to again convert the format to parquet.

![{9C578750-C048-48A0-B7B5-C5FC15AEEEC2}](https://github.com/user-attachments/assets/642da6cb-8703-40c0-ad7c-e80ce1dbbd10)

Then a crawler was excecuted to create the catalog for this bucket and other more. We use a crawler for the raw referenced data(Parquet). This will allows to create tables that can be used in athena.

![{67F6B077-AD8F-4E2E-9E7A-528A02D2B9F2}](https://github.com/user-attachments/assets/6fefc1fc-b699-4916-97b7-4e3450d4a190)

Once the cleaned version has the full data the next bucket is added for the analytics layer

![{B86DCA16-A293-456F-899E-BAE1C332D7F2}](https://github.com/user-attachments/assets/beef83e9-bf48-4b03-8a0c-9cf7f747e60c)

For this a new job was created that merged the two tables into a single one and put it into the analytics buckets.

![{F1FB5F5F-9371-4CEC-A3CD-B95F080C39AC}](https://github.com/user-attachments/assets/1c620450-42a3-4b1e-8025-e7fec44c9c44)


