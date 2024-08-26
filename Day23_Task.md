
# Day 23: Installing Docker on App Server 1

## Task
The Nautilus DevOps team is working on containerizing various applications. As part of this initiative, Docker needs to be installed and configured on App Server 1.

### Specifications:
- Install the `docker-ce` and `docker-compose` packages on App Server 1.
- Start the Docker service after installation.

## Steps:

1. **Install Docker Packages:**
   - Use `yum` to install the necessary Docker packages:
     ```sh
     sudo yum install docker-ce docker-ce-cli containerd.io -y
     sudo yum install docker-compose -y
     ```

2. **Start the Docker Service:**
   - Start the Docker service to enable container management:
     ```sh
     sudo systemctl start docker
     ```

3. **Enable Docker to Start on Boot:**
   - Ensure Docker starts automatically on system boot:
     ```sh
     sudo systemctl enable docker
     ```

## Command Explanation:
- **yum install:** Installs specified packages on a CentOS/RHEL-based system.
- **systemctl start:** Starts the specified service.
- **systemctl enable:** Enables the service to start at boot.

