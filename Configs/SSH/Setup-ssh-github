Setting up SSH keys for GitHub is a secure and convenient way to authenticate when you're working with repositories. Here's how you can set up SSH keys on your machine and add them to your GitHub account:

### 1. Generate a New SSH Key
First, you need to generate a new SSH key on your machine if you don't already have one. Open your terminal and run:

```sh
ssh-keygen -t ed25519 -C "your_email@example.com"
```

- If you are using an older system that doesn't support the `ed25519` algorithm, use `rsa` instead:

```sh
ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
```

- This command creates a new SSH key, using the provided email as a label.

### 2. Save the Key
You'll be prompted to save the key to a specific location:

```sh
Generating public/private ed25519 key pair.
Enter file in which to save the key (/home/your_user/.ssh/id_ed25519):
```

- Press Enter to accept the default file location.

### 3. Set a Passphrase (Optional)
Next, you'll be asked to enter a passphrase:

```sh
Enter passphrase (empty for no passphrase):
Enter same passphrase again:
```

- A passphrase adds an extra layer of security.

### 4. Add the SSH Key to the SSH Agent
Start the SSH agent in the background and add your SSH key:

```sh
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_ed25519
```

### 5. Add the SSH Key to Your GitHub Account
Now, you need to add the SSH key to your GitHub account.

1. Copy the SSH key to your clipboard:

```sh
cat ~/.ssh/id_ed25519.pub
```

- If you are using `rsa`, the command will be `cat ~/.ssh/id_rsa.pub`.

2. Log in to your GitHub account and go to **Settings**.
3. In the "Access" section of the sidebar, click **SSH and GPG keys**.
4. Click **New SSH key** or **Add SSH key**.
5. Paste your key into the "Key" field and add a descriptive label.

### 6. Test the Connection
To make sure everything is set up correctly, you can test your SSH connection:

```sh
ssh -T git@github.com
```

- You should see a success message similar to:

```sh
Hi username! You've successfully authenticated, but GitHub does not provide shell access.
```

### Summary
1. Generate an SSH key using `ssh-keygen`.
2. Save the key and optionally set a passphrase.
3. Start the SSH agent and add your key with `ssh-add`.
4. Copy the public key and add it to your GitHub account.
5. Test the connection to ensure everything is working.

If you have any questions or run into issues, feel free to ask!
