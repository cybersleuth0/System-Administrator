
# Day 22: Cleaning Up Git Branches in Project Repository

## Task
The Nautilus developers are engaged in active development on one of the project repositories located at `/usr/src/kodekloudrepos/ecommerce`. During testing, several test branches were created, and now they require cleanup.

### Specifications:
- Delete a branch named `xfusioncorp_ecommerce` from the `/usr/src/kodekloudrepos/ecommerce` Git repository on the Storage server in Stratos DC.

## Steps:

1. **Log in to the Storage Server:**
   ```sh
   ssh natasha@ststor01.stratos.xfusioncorp.com
2. **Navigate to the Project Directory:**
     ```sh
     cd /usr/src/kodekloudrepos/ecommerce/
     ```

3. **Check the Existing Branches:**
     ```sh
     git branch
     ```

4. **Configure Safe Directory:**
     ```sh
     git config --global --add safe.directory /usr/src/kodekloudrepos/ecommerce
     ```

5. **Remove the Branch:**
     ```sh
     git branch -d xfusioncorp_ecommerce
     ```

## Command Explanation:
-   `ssh natasha@ststor01.stratos.xfusioncorp.com`: Connect to the storage server.
-   `cd /usr/src/kodekloudrepos/ecommerce/`: Navigate to the repository directory.
-   `git branch`: List all branches in the repository.
-   `git config --global --add safe.directory /usr/src/kodekloudrepos/ecommerce`: Add the directory to Git's safe list.
-   `git branch -d xfusioncorp_ecommerce`: Delete the specified branch.
