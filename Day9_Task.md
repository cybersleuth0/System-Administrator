
# Day 9: Adjust ACLs for Critical Files

## Task
After conducting a security audit within the Stratos DC, the Nautilus security team discovered misconfigured permissions on critical files. Corrective actions are being taken by the production support team.

### Specifications:
1. The file's user owner and group owner should be set to `root`.
2. Others should possess read-only permissions on the file.
3. User `ravi` must not have any permissions on the file. 
4. User `garrett` should be granted read-only permission on the file.

## Steps:

1. **Log in to App Server 2:**
   ```sh
   ssh your_username@app_server_1_ip
2.  **Set the File's User Owner and Group Owner to Root:**
	```sh
	sudo chown root:root /etc/hosts
3.  **Ensure Others Have Read Only Permissions:**
	```sh
	sudo chmod 644 /etc/hosts
4. **Remove All Permissions for User Ravi:**
    ```sh
	sudo setfacl -m u:ravi:0 /etc/hosts
5. **Grant Read Only Permission to User Garrett:**
	```sh
	sudo setfacl -m u:garrett:r /etc/hosts
6. **Verify the ACLs:**
	```sh
	getfacl /etc/hosts
7. **Command Explanation:**
	```sh
	ssh your_username@app_server_1_ip: Log in to Nautilus App 1 using your username.
	
	sudo chown root:root /etc/hosts: Set the file's user owner and group owner to root.
	  - sudo: Execute the command with superuser privileges.
	  - chown root:root: Change the file's user and group owner to root.
	  - /etc/hosts: The file to modify.
	sudo chmod 644 /etc/hosts: Ensure others have read-only permissions.
	  - sudo: Execute the command with superuser privileges.
	  - chmod 644: Set the file permissions to `rw-r--r--`.
	  - /etc/hosts: The file to modify.
	sudo setfacl -m u:ravi:0 /etc/hosts: Remove all permissions for user ravi.
	  - sudo: Execute the command with superuser privileges.
	  - setfacl -m: Modify the ACLs.
	  - u:ravi:0: Set no permissions for user ravi.
	  - /etc/hosts: The file to modify.
	sudo setfacl -m u:garrett:r /etc/hosts: Grant read-only permission to user garrett.
	  - sudo: Execute the command with superuser privileges.
	  - setfacl -m: Modify the ACLs.
	  - u:garrett:r: Set read-only permission for user garrett.
	  - /etc/hosts: The file to modify.
	getfacl /etc/hosts: Verify the ACLs of the file.
	  - getfacl: Get file ACLs.
	  - /etc/hosts: The file to check.
