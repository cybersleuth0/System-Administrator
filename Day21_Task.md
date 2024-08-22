
# Day 21: Adding and Committing a Sample File to a Git Repository

## Task
The Nautilus development team needs to incorporate a sample `index.html` file into the recently cloned `beta.git` repository on the Storage server.

### Specifications:
- Copy the sample `index.html` file from the jump host to the Storage server.
- Add and commit the file to the `beta.git` repository located at `/usr/src/kodekloudrepos/beta`.
- Push the changes to the master branch.

## Steps:

1. **Copy the `index.html` File from the Jump Host:**
   - Use the `scp` command to securely copy the sample `index.html` file from the jump host to the Storage server:
     ```sh
     scp /tmp/index.html your_username@storage_server_ip:/usr/src/kodekloudrepos/beta/
     ```

2. **Log in to the Storage Server:**
   - SSH into the Storage server:
     ```sh
     ssh your_username@storage_server_ip
     ```

3. **Navigate to the `beta` Repository:**
   - Change directory to the `beta` repository:
     ```sh
     cd /usr/src/kodekloudrepos/beta
     ```

4. **Add the `index.html` File to the Repository:**
   - Add the file to the repository:
     ```sh
     git add index.html
     ```

5. **Commit the Changes:**
   - Commit the changes with an appropriate commit message:
     ```sh
     git commit -m "Add sample index.html file"
     ```

6. **Push the Changes to the Master Branch:**
   - Push the committed changes to the remote `master` branch:
     ```sh
     git push origin master
     ```

## Command Explanation:
- **scp:** Securely copies files between hosts over SSH.
- **git add:** Stages changes for the next commit.
- **git commit:** Records changes to the repository.
- **git push:** Uploads local repository content to a remote repository.
