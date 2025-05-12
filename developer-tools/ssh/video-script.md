# Video Script: Connecting to a WordPress.com Site Using SSH

---

## **Introduction**

Welcome! In this tutorial, you'll learn how to connect to your WordPress.com site using SSH. We'll cover:

- Enabling SSH access on your site
- Connecting to SSH for the first time
- Generating and using SSH keys for passwordless authentication

Let's get started!

---

## **1. Enabling SSH on a WordPress.com Site**

Before you can connect via SSH, you need to enable SSH access and create your credentials. Note: SSH access is only available for sites on the WordPress.com Business or Commerce plan[1][2].

**Steps:**

- Log into your WordPress.com dashboard and navigate to your site’s *Settings* page.
    - If you use the Classic admin style: go to *Hosting → Site Settings*
    - If you use the Default style: go to *Settings → Server Settings*[2]
- Click the **SFTP/SSH** tab.
- Click **Create credentials**. This generates your SSH username and password for the site. Save these credentials somewhere safe.
    - If you’ve already created credentials, they’ll be displayed. You can use **Reset password** to generate a new one if needed.
- Below the password, find **SSH Access** and toggle **Enable SSH access to this site**.
- Once enabled, a connection command will appear. Copy this command - you’ll use it to connect from your terminal[2].

---

## **2. Connecting to SSH for the First Time**

Now that SSH is enabled and you have your credentials, let’s connect.

### **On macOS and Linux:**

- Open your terminal application.
    - On macOS: *Applications → Utilities → Terminal*
    - On Linux: Open your preferred terminal app[3]
- Paste the SSH command you copied earlier. It looks like:
  ```
  ssh username.wordpress.com@ssh.wp.com
  ```
- Press Enter. The first time you connect, you may be asked to confirm the host's authenticity. Type `yes` and press Enter.
- Enter your SSH password when prompted. Note: You won’t see the password as you type - this is normal.
- If successful, you’re connected and can run shell or WP-CLI commands[3].

### **On Windows:**

- For Windows 10 and newer, you can use the built-in OpenSSH client or Windows Subsystem for Linux. See Microsoft’s documentation for details.
- Alternatively, use [PuTTY](https://www.putty.org/):
    - Download and install PuTTY.
    - Open PuTTY and set:
        - Host Name: `ssh.wp.com`
        - Port: `22`
    - Click **Open**. If prompted to trust the host, click **Yes**.
    - Enter your SSH username and press Enter.
    - Enter your SSH password.
    - You should now be connected[3].

---

## **3. Generating an SSH Key for Passwordless Authentication**

SSH keys let you connect securely without entering your password each time. Here’s how to set them up[4]:

### **A. Generate an SSH Key Pair**

#### **On macOS and Linux:**

- Open Terminal.
- Run:
  ```
  ssh-keygen -t ed25519
  ```
- When prompted, enter a file name for your key or press Enter to accept the default.
- Enter a secure passphrase if you want extra protection.

This creates a private and public key in your `.ssh` directory. The public key file ends with `.pub`[4].

#### **On Windows:**

- Open PowerShell or Command Prompt.
- Run:
  ```
  ssh-keygen -t ed25519
  ```
- Accept the default file name or choose your own.
- Enter a secure passphrase if desired.

Your keys will be saved in the chosen location, with the public key ending in `.pub`[4].

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

Citations:
[1] https://ppl-ai-file-upload.s3.amazonaws.com/web/direct-files/attachments/51150879/aaa7538f-d795-417d-bf14-b3c13a4bfec6/01-ssh.md
[2] https://ppl-ai-file-upload.s3.amazonaws.com/web/direct-files/attachments/51150879/99f77264-3acc-44c8-b489-b81fe572c06e/02-enable.md
[3] https://ppl-ai-file-upload.s3.amazonaws.com/web/direct-files/attachments/51150879/d7be81e8-053b-43b7-a918-9accdeb9581a/03-connect.md
[4] https://ppl-ai-file-upload.s3.amazonaws.com/web/direct-files/attachments/51150879/11305465-3769-4d1c-b358-033f894f0b8c/04-generate-ssh-key.md
[5] https://ppl-ai-file-upload.s3.amazonaws.com/web/direct-files/attachments/51150879/aaa7538f-d795-417d-bf14-b3c13a4bfec6/01-ssh.md
[6] https://ppl-ai-file-upload.s3.amazonaws.com/web/direct-files/attachments/51150879/99f77264-3acc-44c8-b489-b81fe572c06e/02-enable.md
[7] https://ppl-ai-file-upload.s3.amazonaws.com/web/direct-files/attachments/51150879/d7be81e8-053b-43b7-a918-9accdeb9581a/03-connect.md
[8] https://ppl-ai-file-upload.s3.amazonaws.com/web/direct-files/attachments/51150879/11305465-3769-4d1c-b358-033f894f0b8c/04-generate-ssh-key.md

---
Answer from Perplexity: pplx.ai/share