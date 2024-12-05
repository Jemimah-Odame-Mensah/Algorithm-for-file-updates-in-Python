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
I first assigned a string containing this file name to the **_import_file_** variable. Then, I use a **_with_** statement to open it. I use the variable **_file_** to store the file while I work with it inside the **_with_** statement. I also assign all of the IP addresses that should be removed to a variable called **_remove_list_**. This is illustrated in the code bellow
