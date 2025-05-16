# Video Script: Connecting to a WordPress.com Site Using SSH

---

## **Introduction**

Hey there and welcome! In this tutorial, you'll learn how to connect to your WordPress.com site using SSH. We'll cover:

- Enabling SSH access on your site
- Connecting to SSH for the first time
- Generating and using SSH keys for passwordless authentication

Let's get started!

---

## Introduction

SSH (or Secure Shell) is a protocol that allows you to securely connect to a server and execute commands. It’s a powerful tool for developers managing WordPress sites. 

Using SSH on WordPress.com hosting, you can perform tasks various tasks including managing files or running WP-CLI commands directly from your terminal.

SSH access is available for sites on the WordPress.com Business or Commerce plan.

## **1. Enabling SSH on a WordPress.com Site**

Before you can connect via SSH, you need to enable SSH access and create your credentials.

- To start, log into your WordPress.com dashboard and navigate to your site’s *Settings* page.
    - If you use the Classic admin style: go to *Hosting → Site Settings*
    - If you use the Default style: go to *Settings → Server Settings*
- Click the **SFTP/SSH** tab.
- Click **Create credentials**. This generates your SSH username and password for the site. Save these credentials somewhere safe.
    - If you’ve already created credentials, they’ll be displayed. You can use **Reset password** to generate a new one if you don't remember what it was.
- Below the password, find **SSH Access** and toggle **Enable SSH access to this site**.
- Once enabled, a connection command will appear. Copy this command because this is what you’ll use to connect from your terminal.

---

## **2. Connecting to SSH for the First Time**

Now that SSH is enabled, and you have your credentials, let’s connect.

### **On macOS and Linux:**

- On macOS and Linux, open your terminal application.
    - On macOS: *Applications → Utilities → Terminal*
    - On Linux: Open your preferred terminal app[3]
- Paste the SSH command you copied earlier. It looks like:
  ```
  ssh username.wordpress.com@ssh.wp.com
  ```
- Press Enter. The first time you connect, you may be asked to confirm the host's authenticity. Type `yes` and press Enter.
- Enter your SSH password when prompted. You won’t see the password as you type - this is normal, and then press Enter.
- If you've entered the correct password, you’ll be connected to your site's secure shell.

### **On Windows:**

For Windows 10 and newer, you can use the built-in [OpenSSH client](https://learn.microsoft.com/en-us/windows/terminal/tutorials/ssh) or [Windows Subsystem for Linux](https://learn.microsoft.com/en-us/windows/wsl/install). Which ever path you follow you'll have a terminal that looks and works similar to macOS and Linux.

Alternatively, if you're on an older Windows version, we recommend the [PuTTY](https://www.putty.org/) SSH client:
    - Once you've downloaded and installed the PuTTY application, open it and set the following:
        - Host Name: `ssh.wp.com`
        - Port: `22`
    - Click **Open**. If prompted to trust the host, click **Yes**.
    - Enter your SSH username and press Enter.
    - Enter your SSH password.
      
If you've entered everything correctly, you’ll be connected to your site's secure shell.

---

## **3. Generating an SSH Key for Passwordless Authentication**

SSH keys let you connect securely without entering your password each time. You create a key pair which comprises of a public key that's stored on the server and a private key that's kept on your computer. When you connect, the server checks if your private key matches the public key. If they match, you’re granted access without needing to enter a password.

Here’s how to set this up:

### **A. Generate an SSH Key Pair**

#### **On macOS and Linux:**

- Open a Terminal and run:
  ```
  ssh-keygen -t ed25519
  ```
- When prompted, enter a file name for your key or press Enter to accept the default file location.
- When Enter a secure passphrase to add want extra protection. 

This creates a private and public key in your `.ssh` directory. The public key file ends with `.pub`.

#### **On Windows:**

- Open PowerShell or Command Prompt.
- Run:
  ```
  ssh-keygen -t ed25519
  ```
- Accept the default file name or choose your own.
- Enter a secure passphrase if desired.

Your keys will be saved in the chosen location, with the public key ending in `.pub`.

---

### **B. Add Your Public SSH Key to Your WordPress.com Account**

- Copy your public SSH key to your clipboard:
    - **macOS:**
      ```
      pbcopy < ~/.ssh/id_ed25519.pub
      ```
    - **Windows:**
      ```
      clip < ~/.ssh/id_ed25519.pub
      ```
    - **Linux:**
      ```
      cat ~/.ssh/id_ed25519.pub
      ```
      Then manually copy the output[4].
- In your WordPress.com dashboard, click your name (top right) to go to *My Profile*.
- Click **Security**.
- Click **SSH Key** in the Security Checklist.
- Paste your public key into the **Public SSH Key** field and click **Save SSH Key**[4].

---

### **C. Attach Your SSH Key to Your Site**

- Go to your site’s *Settings* page:
    - Classic style: *Hosting → Site Settings*
    - Default style: *Settings → Server Settings*
- Click the **SFTP/SSH** tab.
- Use the **SSH Keys** dropdown to select your key.
- Click **Attach SSH Key to Site**[4].

Your SSH key is now set up for your site. When you connect via SSH, you’ll be authenticated automatically using your key - no password required.

---

## **Conclusion**

You’ve now enabled SSH, connected for the first time, and set up SSH keys for secure, passwordless access to your WordPress.com site. For more advanced usage, check out the official WordPress.com developer documentation.

Happy coding!
