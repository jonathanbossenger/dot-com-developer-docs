# SSH

SSH, Secure SHell, allows you to use a terminal application to access the backend of your site and manage certain site files and settings. It also provides access to WP-CLI, which can be used to quickly make site changes and troubleshoot issues.

[Callout - info]

This feature is available on sites with the WordPress.com Business or Commerce plan.

[/Callout]

## Get WordPress.com SSH Credentials and Enable SSH

If you are accessing SSH for the first time, you must create your credentials and enable SSH Access:

1. Visit your site's dashboard and navigate to Hosting → **Overview** (or Settings → **Hosting Configuration** if using the default interface style).
2. Click the Server Settings tab.
3. If prompted, click **Create credentials**. This only needs to be done once and will generate the SSH username and password for the selected site. The credentials will be used for both SFTP and SSH connections.
4. Store the password in a safe place. If lost or forgotten, the Reset password button can be used to generate a new one.
5. Locate **SSH Access** and toggle on the **Enable SSH access to this site** option.
6. Once SSH Access has been enabled, a connection command will appear. This can be copied and pasted into a terminal application. Review our Connect to SSH instructions for more on accessing your site via SSH.

### Reset a SSH Password

If you forget or lose your SFTP/SSH password, you can reset it by returning to "**Server Settings**" tab after selecting your site from the Sites dashboard.

Within the SFTP/SSH credentials section, click **Reset password**.

## Connect to SSH

You will need your SSH username, password, and a terminal program to access your site via SSH. Below are instructions to connect via some of the most common programs.

### How to Connect to SSH on MacOS and Linux

1. Open your computer's terminal application.
   * On MacOS, visit _Applications → Utilities_ on your computer and open the Terminal application.
   * On Linux, please consult your distribution's documentation for more on opening a terminal window. Some versions may refer to the terminal program as a shell, console, or command prompt.
2. Visit your site's dashboard and navigate to Hosting → **Overview** (or Settings → **Hosting Configuration** if using the default interface style).
3. Click on the Server Settings tab and view the **SFTP/SSH credentials** section.
4. Ensure SSH access is enabled and copy the `ssh` command provided for your site. For example, `ssh example.wordpress.com@sftp.wp.com`.
5. Paste or type the `ssh` command into your terminal application and press enter/return.
   * If this is your first time connecting, your terminal may prompt that it cannot establish the authenticity of the host. Type yes and press enter/return to proceed.
6. Your terminal should now prompt you to enter a password. Paste or type in the SSH password provided when creating your SSH credentials and press enter.
   * Note that when entering your password into your terminal application, characters will not appear as you type. This is by design.
   * If your SSH password has been forgotten or lost, it can be reset.
7. If successful, you should now be connected to SSH and can begin running shell and WP-CLI commands.

### How to Connect to SSH on Windows

Recent versions of Windows, starting with 10, have added SSH support via the Windows Subsystem for Linux as well as the OpenSSH client. Please consult Microsoft's official documentation for using these methods.

Another option for both current and older Windows versions of Windows is PuTTY.

1. Download and install the free PuTTY client.
2. Start PuTTY, configure the Host Name and Port settings, and click Open
   * Host Name should be set to `sftp.wp.com`
   * Port should be set to `22`
3. If this is your first time connecting, you may receive a prompt to trust the rsa2 fingerprint and host. Click **Yes**.
4. PuTTY will launch a terminal screen. Enter your SFTP/SSH username and press Enter/return.
5. When prompted, enter your SFTP/SSH password.
6. If successful, you should now be connected to SSH and can begin running shell and WP-CLI commands.

## SSH Key

The instructions below will guide you through the process of adding an SSH Key to your WordPress.com account. Importantly, you'll need to first generate an SSH key, then add the SSH key to your account. Finally you'll attach the SSH key to any sites you'd like to use it with.

You can only add one key per WordPress.com account which you can then attach to multiple sites. Each site can have multiple keys attached, one per privileged user.

If you don't have an SSH Key on your computer, connecting to SSH via password authentication also works.

### Generate an SSH Key

You can generate SSH keys on Mac, Windows, and Linux. Once you create your key, you can then add your public key to your WordPress.com account.

#### Create an SSH Key on MacOS and Linux

To generate an SSH key using macOS, take the following steps:

1. Open the Terminal.
2. Run the command `ssh-keygen -t rsa`.
3. When prompted, enter the name of the file where you wish to store your key or press `Enter` to accept the default file name.
4. When prompted, type a secure passphrase to use with your key.

This will save a public and a private key in the chosen location. The public key, which you'll need for your WordPress.com account in the next step, will include the .pub extension.

#### Create an SSH Key on Windows

To generate an SSH key using Windows, take the following steps:

1. Open PowerShell or cmd prompt.
2. Run the command `ssh-keygen`.
3. When prompted, enter the name of the file where you wish to store your key or press `Enter` to accept the default file name.
4. When prompted, type a secure passphrase to use with your key.

This will save a public and a private key in the chosen location. The public key, which you'll need for your WordPress.com account in the next step, will include the `.pub` extension.

### Add an SSH Key to Your Account

Before adding your SSH key to your WordPress.com account, you need to copy it to your clipboard. There are two ways to do this using your computer terminal:

**Mac**
  ```bash
  pbcopy < ~/.ssh/id_rsa.pub
  ```

**Windows**
  ```bash
  clip < ~/.ssh/id_rsa.pub
  ```

**Linux**
  ```bash
  cat ~/.ssh/id_rsa.pub
  ```

If your SSH public key file uses a different name than the one mentioned above, edit the code to match the filename on your computer.

After copying your public SSH key to your clipboard, you will be able to add it to your account by following these steps:

1. From your WordPress.com dashboard, go to _My Profile_.
2. On the My Profile page, click on _Security_.
3. Click on the **SSH Key** option available in the Security Checklist.
4. Paste your SSH Key to the **Public SSH Key** field.
5. Click on the **Save SSH Key** button.

Importantly, once you add your SSH key to your WordPress.com account, you'll then need to attach it to each site you'd like to use it on.

### Attach an Existing SSH Key to a Site

After adding an SSH Key to your account, it will be necessary to attach it to the site you want to connect via SSH. To attach your SSH Key to a site, follow these steps:

1. Visit your site's dashboard and navigate to Hosting → **Overview** (or Settings → **Hosting Configuration** if using the default interface style).
2. Click the Server Settings tab.
3. Under the **SSH Access** section, use the **SSH Keys** field to select the desired key.
4. Click on the **Attach SSH Key** to Site button.

Once your SSH key is attached to the site, you can use the SSH key when authenticating over SSH.

### Detach a Key from a Site

If you no longer want to connect to a site using your SSH Key, you can detach the key from the site by following these instructions:

1. Visit your site's dashboard and navigate to Hosting → **Overview** (or Settings → **Hosting Configuration** if using the default interface style).
2. Click the Server Settings tab.
3. Under the **SSH Access** section, locate the SSH Key you want to remove.
4. Click on the **Detach** button to remove the key from the site.

The SSH key will still be associated with your WordPress.com account until you remove it.

### Update an Existing SSH Key

Follow the below steps to update your public SSH key:

1. From your WordPress.com dashboard, go to _My Profile_.
2. On the My Profile page, click on _Security_.
3. Click on the **SSH Key** option available in the Security Checklist.
4. Click on the **Update SSH key** button next to the key you wish to update.
5. Paste your updated SSH Key to the **New SSH Public Key** field.
6. Click the **Update SSH Key** button to save changes.

### Remove an Existing SSH Key

Removing an SSH key from your WordPress.com account will also detach it from each site it's associated with. To remove an existing SSH Key from your WordPress.com account, follow these steps:

1. From your WordPress.com dashboard, go to My Profile.
2. On the My Profile page, click on Security.
3. Click on the **SSH Key** option available in the Security Checklist.
4. Click on the Remove SSH Key button displayed beside the existing key.
5. A confirmation message will be displayed. Confirm you want to remove the key by clicking on the OK button.

## Use Shell Commands

> You should be careful with running commands to prevent data loss or damage your site. Make sure to only run commands when you know exactly what they will do.

Extensive resources are available on using the Linux command line. Some popular examples include the following third-party sources:

* [Ubuntu's Command Line for Beginners Tutorial](https://ubuntu.com/tutorials/command-line-for-beginners)
* [freeCodeCamp's Linux Commands Handbook](https://www.freecodecamp.org/news/the-linux-commands-handbook/)
* [LinuxCommand.org](http://linuxcommand.org/)
* [Microsoft's Shell Course](https://learn.microsoft.com/en-us/training/modules/bash-introduction/)

Below are some common commands:

| Command | Description |
|---------|-------------|
| ls | Show a list of the current directory's contents. |
| cd | Change directory. |
| mkdir | Create a new folder/directory. |
| touch | Create a file. |
| rm | Remove a file. |
| cat | Show contents of a file. |
| cp | Copy. |
| mv | Move. |
| pwd | Show current directory. |
| grep | Search for a specific phrase in file/lines. |
| find | Search files and directories. |
| nano | Text editor. |
| history | Show last 50 used commands. |
| clear | Clear the terminal screen. |
| du | Get file size. |
| rsync | Copy files to and from the server. |

## Use WP-CLI

WP-CLI comes preinstalled on WordPress.com and extends the shell to provide WordPress-specific command line tools. You can start running WP-CLI commands once you have connected to SSH.

There are many commands and subcommands that can help with managing and troubleshooting your site. For more on the commands available and how to use them, you can visit our [WP-CLI guide](https://wordpress.com/support/wp-cli/) or the [WordPress.org documentation for WP-CLI](https://developer.wordpress.org/cli/commands/).

## Troubleshooting

If something happens to your site after you've made changes via SSH, you can restore your site from a [Jetpack backup](https://wordpress.com/support/backup/).

If you run a command and something happens you didn't expect, we can help you restore your site to an earlier point from before you ran the command. We will not be able to help you debug your command to make it work as expected.

## Frequently Asked Questions

### Can I get support for using command line tools?

Due to the complex nature of SSH and WP-CLI, we are not able to provide extensive support for using these tools. Happiness Engineers are available to help with issues connecting via SSH but cannot guide you through using commands.

### Are all commands available?

In order to provide a secure and performant environment, WordPress.com may restrict or disable certain shell and WP-CLI commands.

### Can I set my own SSH password?

The username and password are generated by the system automatically. These are unique to each site. If you have multiple sites, you'll need to use multiple usernames and passwords, one for each site.

### Can I have multiple SSH keys?

You can only add one key per WordPress.com account, which you can then attach to multiple sites. Each site can have multiple keys attached, one per privileged user.
