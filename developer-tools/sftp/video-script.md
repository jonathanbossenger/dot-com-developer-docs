## Video Script: Setting Up and Connecting to SFTP on WordPress.com

---

### **Introduction**

Hey everyone! I’m [Your Name], and welcome to today’s tutorial. If you’re looking to manage your WordPress.com site files more efficiently, you’re in the right place. In this video, I’ll walk you through setting up and connecting to SFTP on WordPress.com, so you can securely access, upload, and manage your site files like a pro.

We’ll cover what SFTP is, why it’s useful, how to create your SFTP credentials, set up popular SFTP clients on Windows, macOS, and Linux, and connect to your WordPress.com site. I’ll also share tips, troubleshooting advice, and point you to official resources for deeper dives.

Let’s get started!

---

## **What is SFTP, and Why Use It?**

Before we jump into the setup, let’s quickly talk about SFTP.

SFTP stands for *SSH File Transfer Protocol*. It’s a secure way to transfer files between your computer and your WordPress.com site. Unlike regular FTP, SFTP encrypts your data, keeping your credentials and files safe from prying eyes.

**Why use SFTP with WordPress.com?**
- Securely upload, download, or edit files on your site.
- Manage theme or plugin files (for Business and Commerce plans).
- Troubleshoot issues or restore site content if something goes wrong.

> **Note:** SFTP access is only available for WordPress.com sites on the Business or Commerce plans.

---

## **Creating and Enabling Your SFTP/SSH Credentials**

To use SFTP, you’ll need to create unique SFTP/SSH credentials for your WordPress.com site.

### **Step 1: Access Your Site’s SFTP Settings**

1. Log in to your WordPress.com account.
2. Go to **My Site** → **Settings** → **Hosting Configuration**.
3. Scroll down to the **SFTP/SSH Credentials** section.

### **Step 2: Generate Your Credentials**

- Click **Create SFTP Credentials**.
- You’ll see your:
    - **SFTP Username**
    - **Server/Host Address**
    - **Port Number** (usually 22)
    - **Password** (auto-generated)

> **Tip:** Copy these credentials and store them in a secure password manager. Never share your SFTP password publicly or via email.

**Security Note:**  
Your SFTP credentials are unique to your site. For extra security, you can regenerate your password at any time from this page.

---

## **Setting Up an SFTP Client**

Now, let’s set up an SFTP client so you can connect to your site. I’ll cover two popular options: **FileZilla** and **Cyberduck**.

### **Option 1: FileZilla**

#### **Install FileZilla**

- **Windows & macOS:**
    - Download FileZilla from the official website.
    - Run the installer and follow the prompts.

- **Linux:**
    - Use your package manager:
        - Ubuntu/Debian:
          ```
          sudo apt install filezilla
          ```
        - Fedora:
          ```
          sudo dnf install filezilla
          ```

#### **Configure FileZilla**

1. Open FileZilla.
2. Click **File** → **Site Manager**.
3. Click **New Site** and name it (e.g., “My WordPress.com Site”).
4. Enter the following details:
    - **Host:** Your site’s SFTP server address.
    - **Port:** 22
    - **Protocol:** SFTP – SSH File Transfer Protocol
    - **Logon Type:** Normal
    - **User:** Your SFTP username
    - **Password:** Your SFTP password
5. Click **Connect**.

> **What to Expect:**  
> The first time you connect, FileZilla may ask you to trust the server’s SSH key. This is normal—just confirm to proceed.

---

### **Option 2: Cyberduck**

#### **Install Cyberduck**

- **macOS & Windows:**
    - Download Cyberduck from the official website.
    - Drag the app to your Applications folder (macOS) or run the installer (Windows).

#### **Configure Cyberduck**

1. Open Cyberduck.
2. Click the **Open Connection** button.
3. Select **SFTP (SSH File Transfer Protocol)** from the dropdown.
4. Enter:
    - **Server:** Your SFTP server address
    - **Port:** 22
    - **Username:** Your SFTP username
    - **Password:** Your SFTP password
5. Click **Connect**.

> **Tip:** If you’re prompted about an “unknown host key,” review the fingerprint and accept if it matches what’s shown in your WordPress.com dashboard.

---

## **Connecting to Your WordPress.com Site Using SFTP**

Once your client is set up:

- Click **Connect** in your SFTP client.
- You’ll see your site’s file structure—typically folders like `wp-content`, `plugins`, `themes`, and `uploads`.

**How to Use SFTP:**
- Drag and drop files to upload or download.
- Right-click files to rename, delete, or set permissions.
- Always back up files before making changes!

> **Security Reminder:**  
> Never share your SFTP credentials. When done, disconnect from the server and close the client.

---

## **Troubleshooting & Frequently Asked Questions**

**Common Issues:**

- **Can’t Connect?**
    - Double-check your credentials—copy/paste carefully.
    - Make sure you’re using SFTP (not FTP).
    - Ensure your WordPress.com plan supports SFTP access.

- **Password Not Working?**
    - Regenerate your SFTP password from the dashboard and try again.

- **Permission Denied?**
    - You might be trying to edit restricted files. Stick to the `wp-content` folder for most changes.

> For more troubleshooting tips, check out the official FAQ and troubleshooting documentation.

---

## **Additional Resources**

- **Official Docs:**
    - [WordPress.com SFTP Overview]
    - [How to Find Your Credentials]
    - [SFTP Client Setup Guides]
    - [SFTP FAQ & Troubleshooting]

---

## **Summary & Call to Action**

Today, you learned:

- What SFTP is and why it’s essential for secure file management on WordPress.com.
- How to create and secure your SFTP credentials.
- How to set up and use FileZilla or Cyberduck on any major operating system.
- Where to find help if you get stuck.

If you found this tutorial helpful, please give it a thumbs up, subscribe for more WordPress.com tips, and drop your questions or experiences in the comments below. Check the video description for all the links to official documentation.

Thanks for watching, and happy site building!

---

**References:**
: developer.wordpress.com/docs/developer-tools/sftp/
: developer.wordpress.com/docs/developer-tools/sftp/credentials/
: developer.wordpress.com/docs/developer-tools/sftp/client-setup/
: developer.wordpress.com/docs/developer-tools/sftp/frequently-asked-questions/

---
Answer from Perplexity: pplx.ai/share