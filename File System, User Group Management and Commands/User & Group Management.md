# User & Group Management

**To create users and groups, the sudo command is required**

### User management
  - `sudo useradd (username)` - adds a new user
  - `sudo passwd (username)` - prompts to type a password for the new user
  - `su - (username)` - switches to new user, where s = substitute and u = user
  - `whoami` - verify user you are currently using

### Assigning sudo priviliges to user
1. Exit new user - returning to sudo enabled account
2. `sudo usermod -aG sudo (username)` - to grant permission, where a = append and G = group
3. `sudo deluser (username) sudo` - to revoke sudo permissions

### Group management
  - `cat /etc/group` - view exisiting groups in the linux filesystem
    - prints groups in the format `group:password placeholder:user(s)`
  - `sudo groupadd (groupname)` - add a group.
    - `cat /etc/group | grep (groupname)` - to confirm presence of group
  - `sudo usermod -aG (groupname) (username)` - add new user to a group
    - `groups` - see groups the new user has been added to (command to be executed in account of new user)
  - `sudo gpasswd -d (username) (groupname)` - delete user from a group
     - `groups` - see groups the new user has been added to (command to be executed in account of new user)
  - `sudo groupdel (groupname)` - delete group
     - `cat /etc/group | grep devops` - to confirm presence of group
  - `sudo usermod -aG (group1),(group2) (username)` - add new user to multiple groups
     - `cat /etc/group | grep devops` - to confirm presence of group


