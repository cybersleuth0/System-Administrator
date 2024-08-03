
# Day 7: Archive and Transfer Developer Data

## Task
Within the Stratos DC, the Nautilus storage server hosts a directory named `/data`, serving as a repository for various developers' non-confidential data. Developer Kirsty has requested a copy of their data stored in `/data/kirsty`.

### Specifications:
Create a compressed archive named `kirsty.tar.gz` of the `/data/kirsty` directory. - Transfer the archive to the `/home` directory on the Storage Server.

## Steps:

1. **Log in to each app server as a user with sudo privileges:**
   ```sh
   ssh your_username@app_server_ip
2.  **Create the Compressed Archive:**
	```sh
	sudo tar -czvf /data/kirsty.tar.gz -C /data kirsty
3.  **Transfer the Archive:**
	```sh
	sudo mv /data/kirsty.tar.gz /home/
4. **Verify the Archive:**
	```sh
	ls -l /home/kirsty.tar.gz
5. **Command Explanation:**
    ```sh
    ssh your_username@storage_server_ip: Log in to the Storage Server using your username.
   sudo tar -czvf /data/kirsty.tar.gz -C /data kirsty: Create a compressed archive of the `/data/kirsty` directory.
   - sudo: Execute the command with superuser privileges.
   - tar: Archive utility to create compressed archives.
   - czvf: Options for `tar` (create, compress with gzip, verbose, file name).
   - /data/kirsty.tar.gz: The name and location of the archive file to be created.
   - C /data: Change to the `/data` directory before performing the archiving.
   - kirsty: The directory to be archived.
   sudo mv /data/kirsty.tar.gz /home/: Move the archive file to the `/home` directory.
   ls -l /home/kirsty.tar.gz: Verify the existence of the archive in the `/home` directory.
