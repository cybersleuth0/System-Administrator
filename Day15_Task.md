# Day 15: Configuring Firewall for Backup Utility Web UI

## Task
The Nautilus system admins team has rolled out a web UI application for their backup utility on the Nautilus backup server within the Stratos Datacenter. This application operates on port 5004, and firewalld is active on the server.
### Specifications:
-   Allow all incoming connections on port 5004/tcp.
-   Ensure the zone is set to public.
## Steps:

1. **Log in to Backup Server:**
   ```sh
   ssh your_username@backup_server_ip
2.  **Allow Incoming Connections on Port 5004/tcp:**
	```sh
	sudo firewall-cmd --zone=public --add-port=5004/tcp --permanent
3. **Reload the Firewall to Apply Changes:**
	```sh
	sudo firewall-cmd --reload
4. **Verify the Port is Allowed:**
	```sh
	sudo firewall-cmd --zone=public --list-ports
7. **Command Explanation:**
	```sh
	ssh your_username@backup_server_ip: Log in to the backup server.
	sudo firewall-cmd --zone=public --add-port=5004/tcp --permanent: Allow incoming connections on port 5004/tcp within the public zone.
	sudo firewall-cmd --reload: Reload the firewall to apply the changes.
	sudo firewall-cmd --zone=public --list-ports: Verify that port 5004/tcp is allowed in the public zone.
