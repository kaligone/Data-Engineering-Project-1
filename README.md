# Olympics Data Analytics Azure Data Engineering Project

## Workflow
![image](https://github.com/user-attachments/assets/f9dccf91-d8e2-4177-8d07-2e3ade0dcdf1)

## Methodology 

#### Source Data
* In this we take data from the source : https://www.kaggle.com/datasets/arjunprasadsarkhel/2021-olympics-in-tokyo
* Downloaded and saved into the source data folder in the respository

#### Azure Data Factory 
* Now in order to use the data we need to store it in the Data storage like Azure Blob storage or ADLS Gen 2.
* So to do that we will use ADF pipeline to read it from source and store it in the ADLS gen 2.
##### Pipeline Workflow :
###### Get MetatData activity :
  By using Get MetaData activity we will get the child items in that directory which are basically the folder or files in it using field set option.
###### ForEach activity:
  In these , for each child items in that folder we perform a copy activity inside the for each activity.
  ###### Copy activity :
    Copy activity will be inside the for each activity which take each child item i.e. file in our case and store it in the ADLS gen 2 storage specified.

