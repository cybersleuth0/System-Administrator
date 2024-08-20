
# Day 19: Setting Up a Git Repository

## Task
The Nautilus development team requested the establishment of a new Git repository for their upcoming application development project. Additionally, the DevOps team provided the application development team with a copy of the existing repository on the Storage Server in Stratos DC.


### Specifications:
 1. Install Git on the Storage Server.
 2. Create a bare repository named `/opt/apps.git`. 
 3. Clone the existing repository located at `/opt/media.git` to the `/usr/src/kodekloudrepos` directory without making any modifications.
 ### Steps:

1. **Install Git on the Storage Server**
   ```sh
   sudo yum install git -y
2. **Create a Bare Repository**
   ```sh
   sudo git init --bare /opt/apps.git
3. **Clone the Existing Repository**
   ```sh
   sudo git clone /opt/media.git /usr/src/kodekloudrepos
4. **Command Explanation:**
   ```sh
	sudo yum install git -y: Installs Git using the `yum` package manager.
	sudo git init --bare /opt/apps.git: Initializes a bare Git repository at the specified path.
	sudo git clone /opt/media.git /usr/src/kodekloudrepos: Clones the specified repository to the target directory without altering the repository.
