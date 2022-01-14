# Spotfire-Fundamentals
#### To get kick start please visit Tibco official site : https://www.tibco.com/products/tibco-spotfire/learn/videos.
#### Also @TIBCO-Software-Inc. owns all the Credits for the following content.
#### Please feel free to raise Pull Requests I will be more than happy to merge it out other things as well !!!

##### (Spotfire files ends with .Dxp extension which stands for 'Data Exploration')

### Topics
1) [Setup Data Source](#How-to-setup-Data-Source)
2) [Creating an Information link](#How-to-create-an-Information-link)
3) [How to add column in Information Link](#How-to-add-column-in-Information-Link)
4) [Spotfire Architecture](#Spotfire-Architecture)
5) [Spotfire Automation Service](#Spotfire-Automation-Service)
6) [Spotfire Client](#Spotfire-Client)
7) [Clickable link in spotfire](#Clickable-link-in-spotfire)
8) [Edit transformation in Spotfire](#Edit-transformation-in-Spotfire-once-created)
9)  [Remove Multiple Rows](#Remove-Multiple-rows)
10) [How to make personalized Information Link in spotfire](#personalized-Information-Link-in-spotfire)
11) [Library Administrator](#Library-Admin)
12) [Map Layers in Spotfire](#Map-Layer)
13) [Performance Tuning](#Performance-Tuning)
14) [In DB & In Memory Difference](#In-DB-and-In-Memory-Difference)
15) [Spotfire Mods](#Spotfire-Mods)
16) [Spotfire Alerts](#Spotfire-Alerts)


### How to setup Data Source

Tools > Information Designer > Window (Setup Data Source) > 
1) Name 
2) Database Type from dropdown
3) Connection URL
	a) Server name or its ip where database is located 
	b) Port number
	c) Database name
4) Saved

![image](https://user-images.githubusercontent.com/86184439/127389321-cce54957-8441-4a35-ae63-f4c08ec8c79f.png)

### How to create an information Link
An information link is a database query specifying the columns to be loaded and any filters needed to narrow down the data table prior to creating visualizations in TIBCO Spotfire. In Information Designer, information links are created from building blocks such as columns and filters using joins, calculations and aggregations.

https://docs.tibco.com/pub/sfire-analyst/10.10.0/doc/html/en-US/TIB_sfire-analyst_UsersGuide/id/id_information_links.htm

1) Create a table in database. (so that we can pull it into Spotfire)

![Table](https://user-images.githubusercontent.com/86184439/127391538-14cf3417-af97-4587-93d7-717e7b1bc90a.PNG)

2) We have to create multiple columns in spotfire (using info designer) & have to save it in library, so that spotfire can able to understand it.
Tools > Information Designer > Multiple Columns (start tab) > Select Table from DB (from data source) > Add > save it in library. (See below)

![image](https://user-images.githubusercontent.com/86184439/127389764-97bb4693-6906-4068-b774-6a073b234d44.png)

3) Now go to Tools > Information Designer > Start (tab) > Create Information link > select columns (or folder) from Elements > Add > Save Created Information Link in the library.




![image](https://user-images.githubusercontent.com/86184439/127391394-db7f6b57-9bd7-4846-8214-7eba0f6ad926.png)

### How to add column in Information Link
1) Add column name in database table. Then we will create a column using information designer (start tab) > column.

![new column](https://user-images.githubusercontent.com/86184439/127391729-86bbf03a-944a-4190-859a-fa0494da6bfc.PNG)

2) Now select that column which you have to add from data source.

![image](https://user-images.githubusercontent.com/86184439/127391792-88b90f07-e102-4cf8-ab5d-c3f61a7d977f.png)

3) Now we will open that information link (by double clicking) in which we want to add this column and then add it > save.

![image](https://user-images.githubusercontent.com/86184439/127391838-965e22a4-8eee-4ae5-bf62-c45f008ed71b.png)

### Spotfire Architecture
Please Visit : https://docs.tibco.com/pub/spotfire_server/7.6.0/doc/html/TIB_sfire_server_tsas_admin_help/GUID-24E8A46B-4BB5-4D8C-8F24-FB8D77E8EC63.html

### Spotfire Automation Service
TIBCO Spotfire® Automation Services is a tool that is integrated into TIBCO Spotfire and makes it possible to run automated jobs in TIBCO Spotfire on a server. The Automation Services Job Builder is used to set up files for executing these jobs.
For more please visit : https://docs.tibco.com/products/tibco-spotfire-automation-services-10-2-0

### Spotfire Client
Spotfire end users connect to Spotfire Server using either an installed client or a web client.
Spotfire Analyst, a fully-featured client for working with data sources and creating complex analyses, is installed on a user's local computer.
To facilitate interactive analysis in a web browser, a Web Player service generates visualizations that are displayed in the web browser. Depending on which of two licenses a user has, the web client will have different capabilities. With the Consumer license users can view interactive analyses. With the Business Author license users can also create and edit simple analyses.
Read in Depth about other things related to:
https://docs.tibco.com/pub/spotfire_server/7.6.1/doc/html/tsas_admin_help/GUID-96A0A613-60C1-4952-B2FF-3CC1387E92F9.html

### Clickable link in spotfire 
Go to Columns Properties tab and select that column > Properties Tab > Link Template > {$}
If you have any part of link at the end of and static URL then you can add {$} after that static URL in the link template section of the specific column eg.
www.some_site_name_here.com/345656467/{$}

### Edit transformation in Spotfire once created
Note: The following steps are applicable for lower version of Spotfire in 10+ you can directly edit using Canvas
If there are more than one transformations on a data table and you need to edit any of those transformation, follow the steps below:
1.	Go To Edit >> Data Table Properties.
2.	Select the desired data table inside which the transformation has been added and click on Refresh Data > With Prompt.
3.	A new window will pop up which will allow you to make the desired changes in each of the transformations.

### Remove Multiple rows 
1. Test = Rank(RowId(),"asc",[name]) and then Limit By Test=1 in data table -> For single Column
2. Test = Rank(RowId(),"asc",[name],[Marks]) and then Limit By Test=1 -> For more than one column

### personalized Information Link in spotfire
https://www.youtube.com/watch?v=puc9gjv8_VI

### Library Admin
![image](https://user-images.githubusercontent.com/86184439/127394321-fadfb579-38a3-4c4d-849a-143f8cc2c0b1.png)

### Map Layer
1) Marker Layer: Responible for showing exact point on the map using coordinatesq. Shape, size & color of the marker can be set by the author or based on the data.
2) Feature Layer: Used for highlighting area of map. Usually based on shape file. Visualizations based on countries, states will be done by this.
3) Image Layer: Used if you want to use your image as base layer.
4) Map Layer: Refer to base maps included with the spotfire. Allow users to includes what in the chart like roads & border.
5) WMS Layer: Allow User to use any web map server as base map rather than what spotfire provides.

### Performance Tuning
1) Remove unnecessary columns from the IL & DOD panel.
2) Make use of load on demand feature.

![image](https://user-images.githubusercontent.com/86184439/127395389-5a25c839-99a3-4ce4-a924-0e4644750db0.png)

If you want to show only certain data in the dxp while loading then you can use load on demand which asks for you to define input i.e., columns on which you want to filter out and then the values for that column (fixed or range of values).

Watch Video: https://www.youtube.com/watch?v=-2LypN_vWwI

3) Make use of Prompts.
4) Make efficient IP,JS scripts and remove unused ones.
5) We can convert the entire data set into sbdf format.
6) Load only that Api’s in ironpython which is needed.
7) From Database side you can make use of indexes (especially clustered indexes), Procedures, Functions, Union All instead of Union, caching to load data faster etc.

### In DB and In Memory Difference
https://docs.tibco.com/pub/sfire-cloud/area/doc/html/en-US/TIB_sfire_bauthor-consumer_usersguide/bauthcons/topics/en-US/in-database_and_in-memory_data_loading_in_the_tibco_cloud_spotfire_web_client.html

### Spotfire Mods 
https://www.tibco.com/products/tibco-spotfire/custom-analytics-apps-mods
https://github.com/TIBCOSoftware/spotfire-mods

### Spotfire Alerts
1. https://community.tibco.com/wiki/spotfire-alerting-extension  
2. https://media.tibco.com/video/tibco_120116_tibco_analytics_meetup_segment2/?_ga=2.148257847.1236992129.1632249756-1900137379.1607341484  
3. https://www.youtube.com/watch?v=gBKB6HNq4zc  


### EPAM Documenter Tool
Using this one can easily get each and every details related to any dashboard like visuals details , scripts, document properties , markings etc in a word document. To use this it should be enabled first, let's say it's available in Dev env then you need to go to Tools > DXP Documenter Tool in spotfire client, then you need to browse the sample document template so that tool will recognize how it should come in word & then the dashboard itself (from the library), in case your dashboard is not available in library then you need to first save it in the respective environment in which is enabled & that's all.

To get easier understand see a 1 min Video : https://solutionshub.epam.com/solution/epam-dxp-documenter


