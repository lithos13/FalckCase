# FalckCase
This case takes the top 250 best rated movies and obteinds from that list, the list of movies rated above of 8.1 filmed after 2000 

# Technical Requirements

- Google Chrome Versión 120.0.6099.111 (Build oficial) (64 bits)
- Microsoft® Excel® 2019 MSO (versión 2311 compilación 16.0.17029.20028) de 64 bits

# Automation
According to the requirement this automation was developed as follow:

After analyzing the case, all the required information is located on the top-rated movies page.

![imagen1](https://github.com/lithos13/FalckCase/assets/68198144/51119887-7f49-4797-8ae2-e124da22b377)

It means the automation does not need transactions, and it is not necessary to use the ReFramework template.


Using a new blank process with a sequence activity, we can build the automation for this case.

![image](https://github.com/lithos13/FalckCase/assets/68198144/b2a8a147-8a51-46ce-bd88-9e4ce0fde7d6)


1. We identified a direct URL to access the top 250 best-rated movies. This allows us to access the list directly without navigating through the menu.
   
![image](https://github.com/lithos13/FalckCase/assets/68198144/1fdd0ec2-3261-4dae-a6a2-841d757e6fde)

By using the 'Use Application/Browser' activity, we open the list..

![image](https://github.com/lithos13/FalckCase/assets/68198144/ef787a58-f7b0-4983-b4e1-0ca43ef5e55d)


2. The following step is to obtain the list with the information of
   
![image](https://github.com/lithos13/FalckCase/assets/68198144/1e04d6b8-56be-4aab-b170-f1a7099e5ddc)

To obtain this data, we use Table Extraction 

![image](https://github.com/lithos13/FalckCase/assets/68198144/a46978eb-85a3-4fd7-bb36-204f91bef4e7)

 ![image](https://github.com/lithos13/FalckCase/assets/68198144/32cafcb9-a3a2-4976-9862-dd35b79ad809)

