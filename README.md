# Algorithm for file updates in Python

As part of my cybersecurity training, I worked on automating the process of updating access control files using Python. The scenario involved managing an allow list of IP addresses for a healthcare organization. By creating a Python algorithm, I efficiently updated the allow list by removing IP addresses flagged for restricted access. This project demonstrated my ability to use Python for security file management and access control compliance.

## Project Description

As a security professional working at a healthcare company,  part of my job requires me to regularly update a file that identifies the employees who can access restricted content. The contents of the file are based on who is working with personal patient records. Employees are restricted access based on their IP address. There is an allow list for IP addresses permitted to sign into the restricted subnetwork. There's also a remove list that identifies which employees I must remove from this allow list.
My task is to create an algorithm that uses Python code to check whether the allow list contains any IP addresses identified on the remove list. If so, I will remove those IP addresses from the file containing the allow list.

## Objective

The objective of this project was to automate the process of updating an allow list of IP addresses by removing those flagged in a remove list, ensuring restricted access to sensitive resources is promptly revoked.

### Skills Learned

- Python file handling (**_open_**, **_.read_**, **_.write_**)
- Data conversion and manipulation (**_.split_**, **_.join_**)
- Conditional logic and iteration (for loops, conditionals)
- Access control management
- Algorithm design

## Steps
### 1. Open the file that contains the allow list:
The file that I want to open and read is called **_“allow_list.txt”_**. This file contains IP addresses. 
I first assigned a string containing this file name to the **_import_file_** variable. Then, I use a **_with_** statement to open it. I use the variable **_file_** to store the file while I work with it inside the **_with_** statement. I also assign all of the IP addresses that should be removed to a variable called **_remove_list_**. This is illustrated in the code bellow:

![Python 1](https://github.com/user-attachments/assets/9c19566b-e79d-417c-99fa-dd8bda2efa84) 
*Ref 1: python code*

### 2. Read the file contents:
Next, I use the **_.read()_** method to convert the contents of the allow list file into a string so that I can read them. I then store this string in a variable called **_ip_addresses_**. This is shown below,

![Python 2](https://github.com/user-attachments/assets/93ba1d90-1841-452f-8309-ff7d8fa78ac3)
*Ref 2: python code*


### 3. Convert the string into a list:
In order to remove individual IP addresses from the allow list, the IP addresses need to be in a list format. Therefore, I used the **_.split()_** method to convert the **_ip_addresses_** string into a list.

![Python 3](https://github.com/user-attachments/assets/3464fa6b-79fa-470d-a50f-836a2cbde031)
*Ref 3: python code*


### 4. Iterate through the remove list:
The second list called **_remove_list_** contains all of the IP addresses that should be removed from the **_ip_addresses_** list. To remove them, I first set up the header of a **_for_** loop that will iterate through the **_remove_list_** and used **_element_** as the loop variable.

![Python 4](https://github.com/user-attachments/assets/aabec37d-27c2-46c2-af59-000834e897c0)
*Ref 4: python code*

### 5. Remove IP addresses that are on the remove list:
In the body of the above iterative statement, I added a code that will remove all the IP addresses from the allow list that are also on the remove list. First, I created a conditional that evaluates if the loop variable **_element_** is part of the **_ip_addresses_** list. Then, within that conditional, I applied the **_.remove()_** method to the **_ip_addresses_** list and removed the IP addresses identified in the loop variable **_element_**. Applying the **_.remove()_** method in this way is possible because there are no duplicates in the **_ip_addresses_** list. 

![Python 5](https://github.com/user-attachments/assets/479711eb-8fb7-4aed-b307-96c85a734197)

*Ref 5: python code*

### 6. Update the file with the revised list of IP addresses:
Now that I have removed these IP addresses from the **_ip_address_** variable, I can complete the algorithm by updating the file with this revised list. To do this, I first converted the **_ip_addresses_** list back into a string using the **_.join()_** method. I applied **_.join()_** to the string **_" "_** in order to separate the elements in the file by spacing them. Then, I used another **_with_** statement and the **_.write()_** method to write over the file assigned to the **_import_file_** variable.

![Python 6](https://github.com/user-attachments/assets/5001532b-72a1-4c8c-a518-35e5d66847db)

*Ref 6: python code*

## Summary
I created an algorithm that removes IP addresses identified in a **_remove_list_** variable from the **_"allow_list.txt"_** file of approved IP addresses. This algorithm involved opening the file, converting it to a string to be read, and then converting this string to a list stored in the variable **_ip_addresses_**. I then iterated through the IP addresses in **_remove_list_**. With each iteration, I evaluated if the element was part of the **_ip_addresses list_**. If it was, I applied the **_.remove()_** method to it to remove the element from **_ip_addresses_**. After this, I used the **_.join()_** method to convert the **_ip_addresses_** back into a string so that I could write over the contents of the **_"allow_list.txt"_** file with the revised list of IP addresses.


