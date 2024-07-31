
# Day 4: Create User with Expiry Date

## Task
As part of the temporary assignment to the Nautilus project, a developer named mark requires access for a limited duration. To ensure smooth access management, a temporary user account with an expiry date is needed.

## Specifications:
Create a user named `mark` on App Server 1 in Stratos Datacenter. - Set the expiry date to `2024-03-28` , ensuring the user is created in lowercase as per standard protocol..

## Steps:

1. **Log in to App Server 1:**
   ```sh
   ssh your_username@app_server_1_ip
2.  **Create the User with an Expiry Date:**
	```sh
	sudo useradd -e 2024-03-28 mark
3.  **Verify the User Creation and Expiry Date:**
	```sh
	sudo chage -l mark
4.  **Command Explanation:**
	```sh
	sudo: Execute the command with administrative privileges.
    useradd: Add a new user.
    -e 2024-03-28: Set the account expiry date to 2024-03-28.
    mark: The username of the new user.
