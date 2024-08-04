
# Day 8: Grant Executable Permissions to a Script

## Task
In a bid to automate backup processes, the xFusionCorp Industries sysadmin team has developed a new bash script named `xfusioncorp.sh`. While the script has been distributed to all necessary servers, it lacks executable permissions on App Server 2 within the Stratos Datacenter.

### Specifications:
- Grant executable permissions to the `/tmp/xfusioncorp.sh` script on App Server 2.
- Ensure that all users have the capability to execute it

## Steps:

1. **Log in to App Server 2:**
   ```sh
   ssh your_username@app_server_2_ip
2.  **Grant Read and Execute Permissions:**
	```sh
	sudo chmod 755 /tmp/xfusioncorp.sh
3.  **Verify the Permissions:**
	```sh
	ls -l /tmp/xfusioncorp.sh
	
	You should see:
	-rwxr-xr-x 1 root root 40 Aug  4 05:43 /tmp/xfusioncorp.sh

	
4. **Command Explanation:**
    ```sh
	ssh your_username@app_server_2_ip: Log in to App Server 2 using your username.
	sudo chmod 755 /tmp/xfusioncorp.sh: Grant read and execute permissions to the script for all users.
	- sudo: Execute the command with superuser privileges.
	- chmod: Change the file mode bits.
	- 755: Set the permissions to `rwxr-xr-x`.
	- /tmp/xfusioncorp.sh: The path to the script.
	ls -l /tmp/xfusioncorp.sh: Verify the permissions of the script.

