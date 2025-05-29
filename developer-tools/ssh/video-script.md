# How to connect to your WordPress.com site using SSH

## **Introduction**

Hey there, and welcome to this WordPress.com developer tools video. 

My name is Jonathan, and today we're going to learn how to connect to your WordPress.com site using SSH. 

Let's get started!

## **1. Enabling SSH on a WordPress.com Site**

SSH is available on all WordPress.com Business and eCommerce plans. Before you can connect via SSH, you need to enable SSH access and create your credentials.

- To start, log into your WordPress.com dashboard and navigate to your site's *Settings* page.
    - If you use the Classic admin style: go to *Hosting → Site Settings*
    - If you use the Default style: go to *Settings → Server Settings*
- Click the **SFTP/SSH** tab.
- Click **Create credentials**. This generates your SSH username and password for the site. Save these credentials somewhere safe.
    - If you've already created credentials, they'll be displayed. You can use **Reset password** to generate a new one if you don't remember what it was.
- Below the password, find **SSH Access** and toggle **Enable SSH access to this site**.
- Once enabled, a connection command will appear. Copy this command because this is what you'll use to connect from your terminal.

## **2. Connecting to SSH for the First Time**

Now that SSH is enabled, and you have your credentials, let's connect.

### **On macOS and Linux:**

- On macOS and Linux, find and open the default terminal application.
- Paste the SSH command you copied earlier. It looks like:
  ```
  ssh username.wordpress.com@ssh.wp.com
  ```
- Press Enter. The first time you connect, you may be asked to confirm the host's authenticity. Type `yes` and press Enter.
- Enter your SSH password when prompted. Note: You won't see the password as you type - this is normal.
- If successful, you're connected and can run shell or WP-CLI commands.

### **On Windows:**

- Modern versions of Windows now include Powershell as the default terminal, as well as a terminal ssh client.
- Open PowerShell by search for it in the Start menu, and then paste the same SSH command you copied earlier:
  ```
  ssh username.wordpress.com@ssh.wp.com
  ```
- As with macOS and Linux, you may be prompted to confirm the host's authenticity. Type `yes` and press Enter.
- Enter your SSH password when prompted. Again, you won't see the password as you type.
- If successful, you're connected and can run shell or WP-CLI commands.

If you're using an older version of Windows, you may need to install a third-party SSH client like [PuTTY](https://www.putty.org/).

You can find instructions on how to use PuTTY to connect to SSH in the [PuTTY documentation](https://www.chiark.greenend.org.uk/~sgtatham/putty/docs.html).

## **3. Generating an SSH Key for Passwordless Authentication**

WordPress.com also supports something called SSH Keys that let you connect to SSH more securely. SSH keys are linked to your computer, so you can use them to authenticate without entering a password. 

### **A. Generate an SSH Key Pair**

The first step is to generate an SSH key pair, which by default are stored in the `.ssh` directory for your user. 

A key pair consists of a private key (which is kept on your computer) and a public key (which is shared with the server).

#### **On macOS and Linux:**

- On macOS and Linux Open your Terminal and run:
  ```
  ssh-keygen -t ed25519
  ```
- When prompted, enter a file name for your key or press Enter to accept the default file location.
- You can also enter a secure passphrase if you want to add extra protection. 

This creates the private and public key in your `.ssh` directory. 

#### **On Windows:**

- Open PowerShell.
- Run:
  ```
  ssh-keygen -t ed25519
  ```
- Accept the default file name or choose your own.
- Enter a secure passphrase if desired.

Your keys will be saved in the chosen location, with the public key ending in `.pub`.

#### A note on the SSH passphrase:

If you set a passphrase for your key pair, you'll need to enter it the first time you want to connect using the key in a new terminal session. This is normal, and your computer will remember the passphrase for the session.

### **B. Add Your Public SSH Key to Your WordPress.com Account**

Your public SSH key needs to be added to your WordPress.com account so the server can recognize you.

- First, copy your public SSH key to your clipboard:
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
      Then manually copy the output.
- In your WordPress.com dashboard, click your name (top right) to go to *My Profile*.
- Click **Security**.
- Click **SSH Key** in the Security Checklist.
- Paste your public key into the **Public SSH Key** field and click **Save SSH Key**[4].

### **C. Attach Your SSH Key to Your Site**

Now that your public key is saved in your WordPress.com account, you need to attach it to your site.

- Go to your site's *Settings* page and navigate back to the **SFTP/SSH** tab.
- At the bottom of the pageuUse the **SSH Keys** dropdown to select your key.
- Click **Attach SSH Key to Site**[4].

Your SSH key is now set up for your site. When you connect via SSH, you'll be authenticated automatically using your key. Notice how it askes for the passphrase, but not the SSH password.

## **Conclusion**

In this video you learned how to enable SSH, generate your SSH key and how to connect to SSH to manage your site.

For tips on how to use shell commands, as well as frequently asked questions, check out the [official WordPress.com developer documentation on SSH](https://developer.wordpress.com/docs/developer-tools/ssh/).

While you're there, take a look at the [section on WP CLI](https://developer.wordpress.com/docs/developer-tools/wp-cli/) for details on how to manage all aspects of your WordPress.com site via SSH.

If you enjoyed this video, please give it a like and subscribe to our channel for more WordPress.com developer tools tutorials.