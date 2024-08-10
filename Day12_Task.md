# Day 12: Crontab Access Configuration

## Task
In alignment with security compliance standards, the Nautilus project team has opted to impose restrictions on crontab access. Specifically, only designated users will be permitted to create or update cron jobs.
### Specifications:
- Allow crontab access to `yousuf` user while denying access to the `jerome` user on App Server 2.
## Steps:

1. **Log in to App Server 2**
   ```sh
   ssh your_username@app_server_2_ip
2.  **Allow Crontab Access to User `yousuf`:**
	```sh
	echo "yousuf" | sudo tee -a /etc/cron.allow
3.  **Deny Crontab Access to User `jerome`:**
	```sh
	echo "jerome" | sudo tee -a /etc/cron.deny
4. **Verify the Configuration:**
	```sh
	cat /etc/cron.allow
	cat /etc/cron.deny
5. **Command Explanation:**
	```sh
	ssh your_username@app_server_2_ip: Log in to App Server 2.
	echo "yousuf" | sudo tee -a /etc/cron.allow: Allow crontab access for `yousuf`.
	echo "jerome" | sudo tee -a /etc/cron.deny: Deny crontab access for `jerome`.
	cat /etc/cron.allow: Check if `yousuf` is listed in cron.allow.
	cat /etc/cron.deny: Check if `jerome` is listed in cron.deny.
