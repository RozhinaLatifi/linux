
# Connecting Without Username and Password  
## Using Public & Private Key Authentication

To connect to a server securely **without entering username and password**, follow the steps below:

### 1. Generate SSH Key Pair
Use the following command to create a public and private key:
```bash
ssh-keygen
```

This will create:
- A **private key** (e.g., `~/.ssh/id_rsa`) — **keep this secure**
- A **public key** (e.g., `~/.ssh/id_rsa.pub`) — to be shared with the server

---

### 2. Add Public Key to Server

Copy the public key to the server’s **authorized keys** list:
```bash
ssh-copy-id username@server_ip
```
Or manually append the contents of `id_rsa.pub` to the server’s:
```bash
~/.ssh/authorized_keys
```

✅ **Make sure you are adding it to the correct user’s home directory.**

---

### Notes:

- Every user profile on the server typically has an `.ssh` directory.
- Inside that directory, the `authorized_keys` file defines **who can connect** using key-based authentication.
- Ensure correct permissions:
  ```bash
  chmod 700 ~/.ssh
  chmod 600 ~/.ssh/authorized_keys
  ```
