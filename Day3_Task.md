
# Day 3: Create User with Non-Interactive Shell

## Task
To accommodate the backup agent tool's specifications, the system admin team at xFusionCorp Industries requires the creation of a user with a non-interactive shell.

### Specifications:
- Create a user named `james` with a non-interactive shell on App Server 1.

## Steps:

1. **Log in to App Server 1:**
   ```sh
   ssh your_username@app_server_1_ip
2.  **Check  if  the  User  Exists:**
	```sh
	id  jarod
3.  **Create the User with a Non-Interactive Shell:**
	```sh
	sudo useradd -s /sbin/nologin james
4.  **Verify the User Creation:**
	```sh
	id james
	grep james /etc/passwd
5.  **Command  Explanation:**
	```sh
	sudo: Execute the command with administrative privileges.
	useradd: Add a new user.
	-s /sbin/nologin: Set the user's shell to /sbin/nologin, which is a non-interactive shell.
	james: The username of the new user.
6. **Difference between Interactive and Non-Interactive Shells"**
	<a href="https://ibb.co/44kBfgb"><img src="https://i.ibb.co/L9K4PhT/Screenshot-2024-07-30-110030.png" alt="Screenshot-2024-07-30-110030" border="0"></a>
