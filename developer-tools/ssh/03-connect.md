# Connect to SSH

To connect to your site via SSH, you will need your SSH username, password, server URL, and a terminal program.

When you create your SSH credentials and enable SSH, the SSH/SFTP user interface will generate a connection command for you, which is the command you’ll need to run in the terminal to connect. It contains the username and server URL for you, for example:

`ssh username.wordpress.com@ssh.wp.com`

- `ssh` is the terminal command you run on macOS/Linux systems to connect via SSH
- `username.wordpress.com` is the username to access the site in question
- `ssh.wp.com` is the server URL.

If you haven’t already, create your SSH credentials and enable SSH by following the instructions in this document.

Below are instructions on how to connect using some of the most common terminal programs.

## How to Connect to SSH on macOS and Linux

1. Open your computer's terminal application.
   * On macOS, visit *Applications → Utilities* on your computer and open the terminal application.
   * On Linux, please consult your distribution's documentation for more on opening a terminal window. Some versions may refer to the terminal program as a shell, console, or command prompt.
2. Paste or type the `ssh` command into your terminal application and press enter/return.
   * If this is your first time connecting, your terminal may prompt that it cannot establish the authenticity of the host. Type yes and press enter/return to proceed.
3. Your terminal should now prompt you to enter a password. Paste or type in the SSH password provided when creating your SSH credentials and press enter.
   * Note that when entering your password into your terminal application, characters will not appear as you type. This is by design.
4. If successful, you should now be connected to SSH and can begin running shell and WP-CLI commands.

## How to Connect to SSH on Windows

Recent versions of Windows, starting with 10, have added SSH support via the [Windows Subsystem for Linux](https://learn.microsoft.com/en-us/windows/wsl/) as well as the OpenSSH client. Please consult [Microsoft's official documentation](https://learn.microsoft.com/en-us/windows/wsl/tutorials/linux) for using these methods.

Another option for both current and older Windows versions of Windows is PuTTY.

1. Download and install the free [PuTTY client](https://www.putty.org/).
2. Start PuTTY, configure the Host Name and Port settings, and click Open
   * Host Name should be set to `ssh.wp.com`
   * Port should be set to `22`
3. If this is your first time connecting, you may receive a prompt to trust the rsa2 fingerprint and host. Click **Yes**.
4. PuTTY will launch a terminal screen. Enter your SSH username and press Enter/return.
5. When prompted, enter your SSH password.
6. If successful, you should now be connected to SSH and can begin running shell and WP-CLI commands.
