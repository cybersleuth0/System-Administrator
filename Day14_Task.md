# Day 14: Synchronizing Timezone Settings

## Task
In the daily standup, it was noted that the timezone settings across the Nautilus Application Servers in the Stratos Datacenter are inconsistent with the local datacenter's timezone, currently set to Atlantic/St_Helena.
### Specifications:
- Synchronize the timezone settings on all Nautilus Application Servers to match the local datacenter's timezone (Atlantic/St_Helena).
## Steps:

1. **Log in to Each App Server:**
   ```sh
   ssh your_username@app_server_ip
2.  **Check the Current Timezone:**
	```sh
	timedatectl
3. **Set the Timezone to Atlantic/St_Helena:**
	```sh
	sudo timedatectl set-timezone Atlantic/St_Helena
4. **Verify the Timezone Change:**
	```sh
	timedatectl
5. **Confirm the System Time:**
	```sh
	date
7. **Command Explanation:**
	```sh
	ssh your_username@app_server_ip: Log in to the app server.
	timedatectl: Utility to view and set the system's time and date.
	sudo timedatectl set-timezone Atlantic/St_Helena: Set the system timezone to Atlantic/St_Helena.
	date: Display the current date and time to confirm the system time reflects the new timezone.
