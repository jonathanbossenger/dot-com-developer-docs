# Connect to SSH

You will need your SSH username, password, and a terminal program to access your site via SSH. 

\[Callout block \- info\]

If you have not already created the SSH credentials, see the Enable SSH page for details. 

\[/Callout block\]

Below are instructions to connect via some of the most common programs.

## How to Connect to SSH on MacOS and Linux

1. Open your computer's terminal application.
   * On MacOS, visit _Applications → Utilities_ on your computer and open the Terminal application.
   * On Linux, please consult your distribution's documentation for more on opening a terminal window. Some versions may refer to the terminal program as a shell, console, or command prompt.
2. Visit your site's dashboard and navigate to Hosting → **Overview** (or Settings → **Hosting Configuration** if using the default interface style).
3. Click on the Server Settings tab and view the **SFTP/SSH credentials** section.
4. Ensure SSH access is enabled and copy the `ssh` command provided for your site. For example, `ssh example.wordpress.com@sftp.wp.com`.

![Activated SSH Access toggle displaying sample command: ssh example.wordpress.com@sftp.wp.com](../images/ssh-command-example.png)

5. Paste or type the `ssh` command into your terminal application and press enter/return.
   * If this is your first time connecting, your terminal may prompt that it cannot establish the authenticity of the host. Type yes and press enter/return to proceed.
6. Your terminal should now prompt you to enter a password. Paste or type in the SSH password provided when creating your SSH credentials and press enter.
   * Note that when entering your password into your terminal application, characters will not appear as you type. This is by design.
   * If your SSH password has been forgotten or lost, it can be reset.
7. If successful, you should now be connected to SSH and can begin running shell and WP-CLI commands.

## How to Connect to SSH on Windows

Recent versions of Windows, starting with 10, have added SSH support via the Windows Subsystem for Linux as well as the OpenSSH client. Please consult Microsoft's official documentation for using these methods.

Another option for both current and older Windows versions of Windows is PuTTY.

1. Download and install the free PuTTY client.
2. Start PuTTY, configure the Host Name and Port settings, and click Open
   * Host Name should be set to `sftp.wp.com`
   * Port should be set to `22`

![PuTTY SSH client for Windows](../images/putty-client.png)

3. If this is your first time connecting, you may receive a prompt to trust the rsa2 fingerprint and host. Click **Yes**.
4. PuTTY will launch a terminal screen. Enter your SFTP/SSH username and press Enter/return.
5. When prompted, enter your SFTP/SSH password.
6. If successful, you should now be connected to SSH and can begin running shell and WP-CLI commands. 