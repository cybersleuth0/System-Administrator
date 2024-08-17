
# Day 17: Enhancing Security with SELinux

## Task
Following a security audit, the xFusionCorp Industries security team has opted to enhance application and server security with SELinux.

### Specifications:
- Install the required SELinux packages.
- Permanently disable SELinux for the time being.
- Ensure that no reboot is required immediately, as a scheduled maintenance reboot is planned for tonight.
- Disregard the current status of SELinux via the command line; the final status after the reboot should be disabled.

## Steps:

1. **Log in to App Server 2**
   ```sh
   ssh your_username@app_server_ip
2. **Install SELinux Packages:**
   ```sh
   sudo yum install -y selinux-policy selinux-policy-targeted
3. **Disable SELinux Permanently:**
   ```sh
   sudo setenforce 0
   sudo sed -i 's/^SELINUX=.*/SELINUX=disabled/' /etc/selinux/config
4. **Verify the Configuration:**
   ```sh
   cat /etc/selinux/config
5. **Command Explanation:**
   ```sh
   ssh your_username@app_server_ip: Log in to the app server.
   sudo yum install -y selinux-policy selinux-policy-targeted: Install SELinux packages.
   sudo setenforce 0: Set SELinux to permissive mode for the current session.
   sudo sed -i 's/^SELINUX=.*/SELINUX=disabled/' /etc/selinux/config: Permanently disable SELinux.
   cat /etc/selinux/config: Verify the SELinux configuration file.
