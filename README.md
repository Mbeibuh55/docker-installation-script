

# Docker Installation Script for Ubuntu

This script automates the installation of Docker on Ubuntu systems. It installs the latest stable version of Docker Community Edition (CE) along with its dependencies.

## Instructions

1. **Download the Script**: 
    - Copy the script from [docker.sh](link_to_raw_script) or create a new file with the content.
    
2. **Make the Script Executable**:
    - Open a terminal and navigate to the directory where you saved the script.
    - Run the following command to make the script executable:
      ```bash
      chmod +x docker.sh
      ```

3. **Run the Script**:
    - Execute the script with sudo privileges by running:
      ```bash
      sudo ./docker.sh
      ```

4. **Log out and Log Back In** (or Restart the System):
    - After the script completes execution, log out and log back in (or restart your system) to apply the group membership changes.
    
5. **Verify Docker Installation**:
    - After logging back in, open a terminal and run the following command to verify that Docker has been installed successfully:
      ```bash
      docker --version
      ```
    - You should see output similar to this:
      ```
      Docker version 20.10.8, build 3967b7d
      ```

6. **Start Using Docker**:
    - You can now start using Docker without sudo. Try running a Docker command, such as:
      ```bash
      docker ps
      ```

## Script Overview

- The script performs the following actions:
  - Updates the apt package index.
  - Installs necessary packages to allow apt to use a repository over HTTPS.
  - Adds Docker's official GPG key.
  - Sets up the stable Docker repository.
  - Installs Docker packages.
  - Adds the current user to the `docker` group.
  - Restarts Docker service.

## Notes

- This script is intended for Ubuntu systems. For other distributions, please refer to the official Docker documentation.
- Make sure to review the script and understand its actions before running it on your system.
- Use caution when executing scripts from the internet. Always verify the source of the script.



