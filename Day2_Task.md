
#  Day 2: Group-Based Access Control Implementation

  

##  Task

The system admin team at xFusionCorp Industries has streamlined access management by implementing group-based access control.

  

###  Specifications:

-  Create a group named nautilus_sftp_users across all App servers within the Stratos Datacenter.

-  Add the user jarod into the nautilus_sftp_users group on all App servers. If the user doesn't exist, create it as well.

  

##  Steps:

  

1.  **Log in to Each App Server:** 
	```sh
	ssh your_username@app_server_ip
2.  **Create  the  Group:**
	```sh
	sudo  groupadd  nautilus_sftp_users
3.  **Check  if  the  User  Exists:**
	```sh
	id  jarod
4.  **Create  the  User (if necessary):**
	```sh
	sudo  useradd  jarod 
5.  **Add  jarod  to  the  Group:**
	```sh
	sudo  usermod  -aG  nautilus_sftp_users  jarod
6.  **Verify  the  User  is  in  the  Group:**
	```sh
	groups  jarod
7.  **Command  Explanation:**
	```sh
	sudo:  Execute  the  command  with  administrative  privileges.
	groupadd:  Create  a  new  group.
	id:  Check  if  the  user  exists  and  display  user  information.
	useradd:  Add  a  new  user.
	usermod:  Modify  a  user  account.
	-a:  Append  the  user  to  the  specified  group  without  removing  them  from  others.
	-G  nautilus_sftp_users:  Specify  the  group  to  which  the  user  should  be  added.
	jarod:  The  username  of  the  user  being  modified.
	groups:  Display  the  groups  a  user  belongs  to.
