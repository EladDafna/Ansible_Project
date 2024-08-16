# Ansible Project Overview

## Summary
This project demonstrates the use of Ansible for automating server configurations and software installations. It includes various playbooks that handle tasks such as installing essential tools, setting up an Apache server, and verifying server types.

## Playbooks Explanation

### 1. `ping.yml`
   - **Purpose:** A simple playbook that pings the target hosts to ensure connectivity.
   - **Tasks:** Executes the ping module to check host availability.

### 2. `installs.yml`
   - **Purpose:** Installs essential packages on the target servers.
   - **Tasks:**
     - Installs Python
     - Installs `net-tools`
     - Installs `tree`
     - Installs `htop`

### 3. `install_apache.yml`
   - **Purpose:** Installs Apache on the target server and checks if port 80 is open.
   - **Tasks:**
     - Installs Apache web server
     - Verifies that port 80 is open
     - Uses `any_errors_fatal: true` to halt execution if any error occurs (e.g., port 80 is closed).

### 4. `Server.yml`
   - **Purpose:** Determines the server's operating system (Debian or RedHat).
   - **Tasks:** Displays whether the server is running on Debian or RedHat.

### 5. `servers_new.yml`
   - **Purpose:** Provides an alternative solution to `Server.yml`.
   - **Tasks:** Similar to `Server.yml`, it identifies the server's operating system but uses a different approach.
