
# Day 18: Setting Up a Git Repository

## Task
The Nautilus development team requested the creation of a Git repository for their new application development project.

### Specifications:
- **Install Git**: Use the `yum` package manager to install Git on the Storage Server. 
- **Create a Repository**: Set up a bare repository named `/opt/apps.git` on the Storage Server.
## Steps:

1. **Log in to the Storage Server**
   ```sh
   ssh your_username@app_server_ip
2. **Install Git**
   ```sh
   sudo yum install git -y
3. **Create a Bare Repository**
   ```sh
   sudo git init --bare /opt/apps.git
4. **Verify Repository Creation**
   ```sh
   ls -l /opt/apps.git
5. **Command Explanation:**
   ```sh
-   **ssh your_username@storage_server_ip**: Connects to the Storage Server.
-   **sudo yum install git -y**: Installs Git using `yum` package manager.
-   **sudo git init --bare /opt/apps.git**: Initializes a bare Git repository in `/opt/apps.git`.
-   **ls -l /opt/apps.git**: Lists the contents of the newly created repository to verify its creation.
