# User & Group Management

**To create users and groups, the sudo command is required**

### User management
  - `sudo useradd (username)` - adds a new user
  - `sudo passwd (username)` - prompts to type a password for the new user
  - `su -(username)` - switches to new user, where s = substitute and u = user
  - `whoami` - verify user you are currently using

### Assigning sudo priviliges to user
1. Exit new user - returning to sudo enabled account
2. `sudo usermod -aG sudo (username)` - to grant permission where a = append and G = group
3. `sudo deluser (username) sudo` - to revoke sudo permissions

### Group management


