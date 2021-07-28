# Spotfire-Basics
#### To get kick start please visit Tibco official site : https://www.tibco.com/products/tibco-spotfire/learn/videos.
#### Also @Tibco owns all the Credits for followin content as well.
#### Please feel free to raise Pull Requests I will be more than happy to merge it out other things as well !!!

##### Spotfire files ends with .Dxp extension which stands for 'Data Exploration'

### Topics in this 
[How to setup Data Source](#How-to-setup-Data-Source?)
•	How to create an Information link?
•	How to add column in Information Link?
•	Spotfire Architecture 
•	Spotfire Automation Service
•	Spotfire Client
•	Q & A 
•	Clickable link in spotfire
•	Can we edit transformation once created?
•	Remove Multiple Rows
•	How to make personalized Information Link in spotfire
•	Library Administrator
•	Map Layers in Spotfire 
•	Spotfire Versions
•	Performance Tuning


### How to setup Data Source?

Tools > Information Designer > Window (Setup Data Source) > 
1) Name 
2) Database Type from dropdown
3) Connection URL
	a) Server name or its ip where database is located 
	b) Port number
	c) Database name
4) Save

![image](https://user-images.githubusercontent.com/86184439/127389321-cce54957-8441-4a35-ae63-f4c08ec8c79f.png)

### How to create information Link?
Q. What is information link?
An information link is a database query specifying the columns to be loaded and any filters needed to narrow down the data table prior to creating visualizations in TIBCO Spotfire. In Information Designer, information links are created from building blocks such as columns and filters using joins, calculations and aggregations.

1)	Create table in database.
2)	Now we have to create multiple columns in spotfire (using info designer) & have to save it in library, so that spotfire can able to understand it.
Tools > Information Designer > Multiple Columns (start tab) > Select Table from DB (from data source) > Add > save it in library. (See below)

![image](https://user-images.githubusercontent.com/86184439/127389764-97bb4693-6906-4068-b774-6a073b234d44.png)

