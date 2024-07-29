# Day 2: Group-Based Access Control Implementation

## Task
The system admin team at xFusionCorp Industries has streamlined access management by implementing group-based access control.

### Specifications:
- Create a group named `nautilus_sftp_users` across all App servers within the Stratos Datacenter.
- Add the user `jarod` into the `nautilus_sftp_users` group on all App servers. If the user doesn't exist, create it as well.

## Steps:

1. **Log in to Each App Server:**
   ```sh
   ssh your_username@app_server_ip
   
2. **Create the Group:**
  ```sh
  sudo groupadd nautilus_sftp_users
