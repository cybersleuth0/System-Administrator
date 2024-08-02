
# Day 6: Steps to Disable Direct SSH Root Login

## Task
After doing some security audits of servers, xFusionCorp Industries security team has implemented some new security policies. One of them is to disable direct root login through SSH. Disable direct SSH root login on all app servers in Stratos Datacenter.

## Steps:

1. **Log in to each app server as a user with sudo privileges:**
   ```sh
   ssh your_username@app_server_ip
2.  **Open the SSH configuration file (`/etc/ssh/sshd_config`) with a text editor:**
	```sh
	sudo vi /etc/ssh/sshd_config
3.  **Find the line that says `PermitRootLogin`. If it is commented out (preceded by a `#`), uncomment it by removing the `#`. Then, change its value to `no`:**
	```sh
	PermitRootLogin no
4. **Save the file and exit the text editor. If you are using `vi`, you can do this**
     ```sh
     :wq
5. **Restart the SSH service to apply the changes:**
	```sh
	sudo systemctl restart sshd
6. **Verify the Configuration:**
   ```sh
   ssh root@app_server_ip
   You should see a message indicating that the login is denied:
   
   Permission denied, please try again.
 7. **Command Explanation:**
    ```sh
    ssh your_username@app_server_ip: Log in to the server using a user with sudo privileges.
    sudo nano /etc/ssh/sshd_config: Open the SSH configuration file in the nano text editor with superuser privileges.
    PermitRootLogin no: Disable direct root login via SSH.
    sudo systemctl restart sshd: Restart the SSH service to apply the changes.
    ssh root@app_server_ip: Attempt to log in as the root user to verify that the direct login is disabled.
