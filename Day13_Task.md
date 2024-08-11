# Day 13: Enabling GUI Boot by Default

## Task
With the installation of new tools on the app servers within the Stratos Datacenter, certain functionalities now necessitate graphical user interface (GUI) access.
### Specifications:
- Adjust the default runlevel on all App servers in Stratos Datacenter to enable GUI booting by default. 
- Ensure no server reboot is initiated after completing this task.
## Steps:

1. **Log in to App Server 2**
   ```sh
   ssh your_username@app_server_ip
2.  **Set the Default Runlevel to GUI:**
	```sh
	sudo systemctl set-default graphical.target
3. **Verify the Configuration:**
	```sh
	systemctl get-default
5. **Command Explanation:**
	```sh
	ssh your_username@app_server_ip: Log in to the app server.
	sudo systemctl set-default graphical.target: Set the default boot target to GUI.
	systemctl get-default: Verify that the default boot target is set to GUI.
