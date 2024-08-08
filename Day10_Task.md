
# Day 10: String Substitution in XML Files

## Task
Within the Stratos DC, the backup server holds template XML files crucial for the Nautilus application. Before utilization, these files require valid data insertion. As part of routine maintenance, system admins at xFusionCorp Industries employ string and file manipulation commands.

### Specifications:
- Substitute all occurrences of the string `Sample` with `Cloud` within the XML file located at `/root/nautilus.xml` on the backup server.

## Steps:

1. **Log in to App Server 2:**
   ```sh
   ssh your_username@backup_server_ip
2.  **Substitute All Occurrences of "Sample" with "Cloud":**
	```sh
	sudo sed -i 's/Sample/Cloud/g' /root/nautilus.xml
3.  **Verify the Changes:**
	```sh
	sudo grep 'Sample' /root/nautilus.xml
4. **Command Explanation:**
	```sh
	ssh your_username@backup_server_ip: Log in to the backup server using your username.
	sudo sed -i 's/Sample/Cloud/g' /root/nautilus.xml: Substitute all occurrences of "Sample" with "Cloud" in the specified file.
	 - sudo: Execute the command with superuser privileges.
	 - sed: Stream editor for filtering and transforming text.
	 - -i: Edit files in place.
	 - s/Sample/Cloud/g: Substitute (`s`) all occurrences (`g`) of "Sample" with "Cloud".
	 - /root/nautilus.xml: The path to the XML file.
	sudo grep 'Sample' /root/nautilus.xml: Verify the changes by searching for any remaining instances of "Sample".
	 - grep: Search for text in the file.
	 - 'Sample': The string to search for.
	 - /root/nautilus.xml: The file to search within.
