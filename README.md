# FalckCase
This case involves obtaining the list of the top 250 best-rated movies and, from that list, extracting the movies rated above 8.1 filmed after 2000. 

# Technical Requirements

- Google Chrome Versión 120.0.6099.111 (Build oficial) (64 bits)
- Microsoft® Excel® 2019 MSO (versión 2311 compilación 16.0.17029.20028) de 64 bits

# Automation
According to the requirements, this automation was developed as follows:

After analyzing the case, all the required information is located on the top-rated movies page.

![image](https://github.com/lithos13/FalckCase/assets/68198144/88bf5f1b-efa1-4ebf-ada1-0ca5a7847f2e)


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

![image](https://github.com/lithos13/FalckCase/assets/68198144/0f12b86a-e590-45e6-87bf-adf043097b3b)


> [!NOTE]
> The linQ uses Regular expressions to clean the title



4. Similarly, let's clean the rate data by cloning the data table once again, as we are going to modify the data once more.

![image](https://github.com/lithos13/FalckCase/assets/68198144/596b23d3-0f42-4ac3-b734-aa53619cabc5)


5. After cleaning the data, let's move on to create a filter that gives us only the movies filmed after the year 2000.
   By using the 'Filter DataTable' activity as shown in the following image:

   ![image](https://github.com/lithos13/FalckCase/assets/68198144/8bcbb45f-4252-47d3-83a7-9422da77049f)



6. If the previous filter provides us with a list of movies, let's apply the filter for movies rated above 8.1
   In this case, we use LINQ because the rate column needs to be handled as a Double in order to make the comparison.

   ![image](https://github.com/lithos13/FalckCase/assets/68198144/954439e8-c4dd-419c-b008-dd76ad80b2ed)


7. Finally, after applying the filters and if there are movies in the list, let's save the results in an Excel file
   
   ![image](https://github.com/lithos13/FalckCase/assets/68198144/6350ed3a-3353-45aa-8a85-e26bfa942549)

   ![image](https://github.com/lithos13/FalckCase/assets/68198144/3e85ebf1-7266-46eb-b1c0-368b0c5c8284)
