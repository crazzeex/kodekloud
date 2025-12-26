# Creating a user with a non-interactive shell on a server
1. Access the server - can be via ssh
2. `sudo useradd -s /sbin/nologin ammar` (-s is for shell, nologin for non-interactive, ammar is the username)