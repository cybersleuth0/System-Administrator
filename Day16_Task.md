# Day 16: Enforcing Process Limits on Storage Server

## Task
In the Stratos Datacenter, our Storage server is encountering performance degradation due to excessive processes held by the `nfsuser` user. To mitigate this issue, we need to enforce limitations on its maximum processes.
### Specifications:
-   Set the soft limit to `1025`.
-   Set the hard limit to `2025`.
## Steps:

1. **Log in to the Storage Server:**
   ```sh
   ssh your_username@storage_server_ip
2.  **Edit the Limits Configuration File Using vi:**
	```sh
	sudo vi /etc/security/limits.conf
- Press `i` to enter insert mode, then add:
3. **Add the Following Lines to the File:**
	```sh
	nfsuser soft nproc 1025
	nfsuser hard nproc 2025
4. **Save and Exit the vi Editor:**
	```sh
	Press `Esc`, then type `:wq` and press `Enter` to save and exit.
5. **Verify the Changes:**
	```sh
	ulimit -a -u nfsuser
6. **Command Explanation:**
	```sh
	ssh your_username@storage_server_ip: Log in to the storage server.
	sudo vi /etc/security/limits.conf: Open the limits configuration file in vi editor.
	nfsuser soft nproc 1025: Set the soft process limit for nfsuser to 1025.
	nfsuser hard nproc 2025: Set the hard process limit for nfsuser to 2025.
	ulimit -a -u nfsuser: Verify the current process limits for nfsuser.
