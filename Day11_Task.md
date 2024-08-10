
# Day 11: Secure File Transfer between Servers

## Task
A Nautilus developer has stored confidential data on the jump host within Stratos DC. To ensure security and compliance, this data must be transferred to one of the app servers.

### Specifications:
- Copy the `/tmp/nautilus.txt.gpg` file from the jump server to App Server 2, placing it in the `/home/webapp` directory.
## Steps:

1. **Log in to the Jump Server:**
   ```sh
   ssh your_username@jump_server_ip
2.  **Copy the File to App Server 2:**
	```sh
	scp /tmp/nautilus.txt.gpg your_username@app_server_2_ip:/home/webapp/
3.  **Verify the File on App Server 2:**
	```sh
	ssh your_username@app_server_2_ip
	ls -l /home/webapp/nautilus.txt.gpg
4. **Command Explanation:**
	```sh
	ssh your_username@jump_server_ip: Log in to the jump server.
	scp /tmp/nautilus.txt.gpg your_username@app_server_2_ip:/home/webapp/: Securely copy the file to App Server 2.
	 - scp: Secure copy command.
	 - /tmp/nautilus.txt.gpg: The file to transfer.
	 - your_username@app_server_2_ip: Your username and App Server 2's IP address.
	 - /home/webapp/: The destination directory.
	ssh your_username@app_server_2_ip: Log in to App Server 2.
	ls -l /home/webapp/nautilus.txt.gpg: Verify the file was transferred.
