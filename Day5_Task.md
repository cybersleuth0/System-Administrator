
# Day 5: Filter and Relocate User Data

## Task
Due to an accidental data mix-up, user data was unintentionally mingled on Nautilus App Server 3 at the /home/usersdata location by the Nautilus production support team in Stratos DC. To rectify this, specific user data needs to be filtered and relocated.

### Specifications:
- Locate all files (excluding directories) owned by user `kirsty` within the `/home/usersdata` directory on App Server 3.
- Copy these files while preserving the directory structure to the `/news` directory.

## Steps:

1. **Log in to App Server 3:**
   ```sh
   ssh your_username@app_server_3_ip
2.  **Locate and Copy Files Owned by `kirsty` to `/news` Directory:**
	```sh
	sudo find /home/usersdata -type f -user kirsty -exec cp --parents {} /news \;
3.  **Verify the User Creation and Expiry Date:**
	```sh
	sudo find /home/usersdata -type f -user kirsty -exec cp --parents {} /news \;
4.  **Command Explanation:**
	```sh
	sudo: Execute the command with administrative privileges.
    find /home/usersdata -type f -user kirsty: Locate all files (excluding    directories) in /home/usersdata owned by the user kirsty.
    -exec cp --parents {} /news \;: Copy each found file to the /news directory while preserving the directory structure.
    --parents: Preserve the directory structure when copying files.{}: Placeholder  for the current file found by find.
    \;: End of the exec command.
