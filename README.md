# FalckCase
This case involves obtaining the list of the top 250 best-rated movies and, from that list, extracting the movies rated above 8.1 filmed after 2000. 

# Technical Requirements

- Google Chrome Versión 120.0.6099.111 (Build oficial) (64 bits)
- Microsoft® Excel® 2019 MSO (versión 2311 compilación 16.0.17029.20028) de 64 bits

# Automation
According to the requirements, this automation was developed as follows:

After analyzing the case, all the required information is located on the top-rated movies page.

![imagen1](https://github.com/lithos13/FalckCase/assets/68198144/51119887-7f49-4797-8ae2-e124da22b377)

It means the automation does not need transactions, and it is not necessary to use the ReFramework template.


By using a new blank process with a sequence activity, we can build the automation for this case.

![image](https://github.com/lithos13/FalckCase/assets/68198144/b2a8a147-8a51-46ce-bd88-9e4ce0fde7d6)




1. We identified a direct URL to access the top 250 best-rated movies. This allows us to access the list directly without navigating through the menu.
   
![image](https://github.com/lithos13/FalckCase/assets/68198144/1fdd0ec2-3261-4dae-a6a2-841d757e6fde)

By using the 'Use Application/Browser' activity, we open the list..

![image](https://github.com/lithos13/FalckCase/assets/68198144/ef787a58-f7b0-4983-b4e1-0ca43ef5e55d)



2. The following step is to obtain the list with the information of:
   
![image](https://github.com/lithos13/FalckCase/assets/68198144/1e04d6b8-56be-4aab-b170-f1a7099e5ddc)

To obtain this data, we use table extraction and save it in the 'dt_top250Movies' data table.

![image](https://github.com/lithos13/FalckCase/assets/68198144/a46978eb-85a3-4fd7-bb36-204f91bef4e7)

![image](https://github.com/lithos13/FalckCase/assets/68198144/32cafcb9-a3a2-4976-9862-dd35b79ad809)



3. Once the data is obtained, we need to clean the information for the title and rate because they come with additional information like this:

![image](https://github.com/lithos13/FalckCase/assets/68198144/45dc87b6-4a96-4936-9780-c81a287df1d5)

By using LINQ, let's remove the numbers from the title. Since we are going to change the data table's data, we need to clone the 'dt_top250Movies' in order to avoid errors.

![image](https://github.com/lithos13/FalckCase/assets/68198144/74b168a7-f227-4889-a933-08c92df5db4a)

the linQ uses Regular expressions to clean the title



