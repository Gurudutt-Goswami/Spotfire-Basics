# Spotfire-Basics
#### To get kick start please visit Tibco official site : https://www.tibco.com/products/tibco-spotfire/learn/videos.
#### Also @TIBCO-Software-Inc. owns all the Credits for followin content as well.
#### Please feel free to raise Pull Requests I will be more than happy to merge it out other things as well !!!

##### Spotfire files ends with .Dxp extension which stands for 'Data Exploration'

### Topics in this 
1) [How to setup Data Source](#How-to-setup-Data-Source?)
2) [How to create an Information link?](#How-to-create-an-Information-link?)
3) How to add column in Information Link?
4) Spotfire Architecture
5) Spotfire Automation Service
6) Spotfire Client
7) Q & A 
8) Clickable link in spotfire
9) Can we edit transformation once created?
10) Remove Multiple Rows
11) How to make personalized Information Link in spotfire
12) Library Administrator
13) Map Layers in Spotfire 
14) Spotfire Versions
15) Performance Tuning


### How to setup Data Source?

Tools > Information Designer > Window (Setup Data Source) > 
1) Name 
2) Database Type from dropdown
3) Connection URL
	a) Server name or its ip where database is located 
	b) Port number
	c) Database name
4) Saved

![image](https://user-images.githubusercontent.com/86184439/127389321-cce54957-8441-4a35-ae63-f4c08ec8c79f.png)

### How to create information Link?
Q. What is information link?
An information link is a database query specifying the columns to be loaded and any filters needed to narrow down the data table prior to creating visualizations in TIBCO Spotfire. In Information Designer, information links are created from building blocks such as columns and filters using joins, calculations and aggregations.

1) Create a table in database. (so that we can pull it into Spotfire)
![Table](https://user-images.githubusercontent.com/86184439/127391538-14cf3417-af97-4587-93d7-717e7b1bc90a.PNG)

2) We have to create multiple columns in spotfire (using info designer) & have to save it in library, so that spotfire can able to understand it.
Tools > Information Designer > Multiple Columns (start tab) > Select Table from DB (from data source) > Add > save it in library. (See below)

![image](https://user-images.githubusercontent.com/86184439/127389764-97bb4693-6906-4068-b774-6a073b234d44.png)
3) Now go to Tools > Information Designer > Start (tab) > Create Information link > select columns (or folder) from Elements > Add > Save Created Information Link in the library.
![image](https://user-images.githubusercontent.com/86184439/127391394-db7f6b57-9bd7-4846-8214-7eba0f6ad926.png)

### How to add column in Information Link?
1) Add column name in database table. Then we will create a column using information designer (start tab) > column.
![new column](https://user-images.githubusercontent.com/86184439/127391729-86bbf03a-944a-4190-859a-fa0494da6bfc.PNG)

2) Now select that column which you have to add from data source.
![image](https://user-images.githubusercontent.com/86184439/127391792-88b90f07-e102-4cf8-ab5d-c3f61a7d977f.png)

3) Now we will open that information link (by double clicking) in which we want to add this column and then add it > save.
![image](https://user-images.githubusercontent.com/86184439/127391838-965e22a4-8eee-4ae5-bf62-c45f008ed71b.png)

### Spotfire Architecture
https://docs.tibco.com/pub/spotfire_server/7.6.0/doc/html/TIB_sfire_server_tsas_admin_help/GUID-24E8A46B-4BB5-4D8C-8F24-FB8D77E8EC63.html

