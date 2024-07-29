# Day 1: Custom Apache User Creation

## Task
In response to heightened security concerns, the xFusionCorp Industries security team has opted for custom Apache users for their web applications. Each user is tailored specifically for an application, enhancing security measures.

### Specifications:
- Create a user named `james` on App Server 3 within the Stratos Datacenter.
- Assign a unique UID `1102` and designate the home directory as `/var/www/james`.

## Steps:

1. **Log in to App Server 3:**
   ```sh
   ssh your_username@app_server_3_ip

2. **Create User And Set Home Dir:**
   ```sh
   sudo useradd -u 1102 -d /var/www/james -m james

3. **Command Explanation:**
   ```sh
    sudo: Execute the command with administrative privileges.
    useradd: Add a new user.
    -u 1102: Assign the user a unique UID of 1102.
    -d /var/www/james: Set the home directory to /var/www/james.
    -m: Create the home directory if it doesn't exist.
    james: The username of the new user.
   
4. **Verify the User Creation:**
  ```sh
    id james
    ls -ld /var/www/james
   

