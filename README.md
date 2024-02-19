# Operation and Usage Instructions

###

Description Section
The purpose of this Python script is to automate the process of adding multiple users and groups to a Linux system. Instead of manually creating each user, the script reads user information from an input file (create-users.input) and performs the necessary configurations to add the users and assign them to specified groups. This automation simplifies and streamlines the user management process, particularly in scenarios where a large number of users need to be added across multiple systems.

Operation Section:

Step 1 - Clone the Repository: 
Clone this GitHub repository to your local machine using the following command:
git clone [https://github.com/yourusername/inet_4031_adduser_script.git](https://github.com/bashirabah/inet_4031_adduser_script.git )

Step 2 - Navigate to the Repository: 
Change directory to the cloned repository:
cd inet_4031_adduser_script

Step 3 - Create Input File: 
Create a text file named create-users.input in the repository directory. Each line in this file should define a user, with fields separated by colons (:). The fields include username, password, last name, first name, and group list. Ensure correct formatting to avoid errors during user creation.

Example:
user1:password1:Doe:John:group1
user2:password2:Smith:Jane:group2,group3

Step 4 - Run the Script: 
Execute the script with elevated privileges using one of the following commands:

sudo ./create-users.py < create-users.input or cat create-users.input | sudo ./create-users.py

This will run the script and create users on your system based on the information provided in the create-users.input file.

Step 5 - Confirmation: 
After running the script, confirm that the users have been created by checking /etc/passwd and /etc/group files using the grep command:

grep username /etc/passwd
grep username /etc/group

Ensure that you have Python installed on your system and have administrative privileges (sudo) to execute the script successfully. 
