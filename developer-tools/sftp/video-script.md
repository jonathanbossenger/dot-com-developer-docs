# How to connect to your WordPress.com site via SSH

## **Introduction**

Hey everyone! I’m Jonathan, and welcome to this video on using SFTP on WordPress.com. 

Today I’ll walk you through setting up and connecting to SFTP on WordPress.com, so you can securely access, upload, and manage your site files like a pro.

Let’s get started!

## **What is SFTP, and Why Use It?**

Before we jump into the setup, let’s quickly talk about SFTP.

SFTP stands for *SSH File Transfer Protocol*. It’s a secure way to transfer files between your computer and your WordPress.com site. Unlike regular FTP, SFTP uses the same protocol as SSH which encrypts your data, keeping your credentials and files safe and secure.

To use SFTP, you’ll need to create unique SFTP credentials for your WordPress.com site.

These credentials are the same as your SSH credentials, so if you’ve already set up SSH, the process is similar.

## **Creating and Enabling Your SFTP/SSH Credentials**

SFTP access is only available for WordPress.com sites on the Business or Commerce plans.

1. To start, log in to your WordPress.com account, and navigate to your site's Settings.
   - If you use the Classic admin style: go to *Hosting → Site Settings*
   - If you use the Default style: go to *Settings → Server Settings*
- Click the **SFTP/SSH** tab.
- Click **Create credentials**. This generates your SFTP/SSH username and password for the site. Save these credentials somewhere safe.
- The important details you’ll need are:
    - The server **URL**
    - The **Port**
    - Your **Username**
    - And your **Password**

Copy these credentials and store them in somewhere or in a password manager. Never share your password publicly or via email.

If you ever forget your password, you can return to the **SFTP/SSH** tab and regenerate your password using the **Reset password** option.

## **Setting Up an SFTP Client**

Now, let’s set up an SFTP client so you can connect to your site. In this video I’ll cover two popular options: **FileZilla** and **Cyberduck**.

### **FileZilla**

FileZilla is a popular, free, and open-source SFTP client that works on all operating systems. You can download it from the FileZilla website.

1. Once installed, open FileZilla and click **File** → **Site Manager**. 
2. Click **New Site** and give the site a name.
3. In the settings panel, change the **Protocol** to **SFTP - SSH File Transfer Protocol**.
4. Enter the **Host:**  and **Port:** values you copied earlier.
5. Under **Logon Type:** select Normal
6. Then enter your username in the **User:** field and your password
7. Finally, click **Connect**.

The first time you connect, FileZilla may ask you to trust the server’s SSH key. This is normal—just confirm to proceed.

Once connected, you’ll see your site’s file structure on the right side of the FileZilla window. You can now drag and drop files to upload or download them.

### **Option 2: Cyberduck**

Cyberduck is another popular SFPT client available both on macOS and Windows. You can download it from the Cyberduck website.

1. After you install and open Cyberduck, click the **New Bookmark** button.
2. In the New Bookmark window, select **SFTP (SSH File Transfer Protocol)** from the dropdown.
3. Give the bookmark a nickname
4. Enter the **Server:** and **Port:** values you copied earlier.
5. Add your **Username:**
6. Enter your **Password:**
7. Close the New Bookmark window and click the bookmark you just created to connect.

**Tip:** If you are asked to accept the server’s fingerprint key, click Allow to proceed.

Once connected, you’ll see your site’s file structure in the Cyberduck window. You can now drag and drop files to upload or download them.

## **Summary**

For more details on enabling and connecting to SFTP, as well as troubleshooting tips, make sure to visit the official WordPress.com developer documentation on SFTP. (https://developer.wordpress.com/docs/developer-tools/sftp)

If you found this tutorial helpful, please give it a like, subscribe for more WordPress.com developer tutorials, and drop your questions and feedback in the comments below. 

Happy coding!