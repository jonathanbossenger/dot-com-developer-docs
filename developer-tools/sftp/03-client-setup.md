# Set Up a Client

An SFTP client is a tool that will accept your credentials and allow you to access your website's files. There are many clients available. If you don't have a preference, we recommend FileZilla. We have provided setup instructions below for several popular FTP clients.

## FileZilla

To access SFTP with FileZilla, take the following steps:

1. [Visit the FileZilla website](https://filezilla-project.org/download.php) to download FileZilla for Windows, MacOS, or Linux.
2. Open the program and navigate to *File → Site Manager*.
3. Click the "**New site**" button.
4. Set the 'Protocol' field to **SFTP (SSH File Transfer Protocol)**, not FTP.
5. Add the credentials (URL [in the Host field], Port, Username, and Password) you obtained [earlier](credentials.md).
6. Click the **Connect** button.

In the default FileZilla layout, you'll see your local files on the left and your site's files on the right.

## Transmit

If you are using macOS, you can use the Transmit app on your computer. You can download the app directly from the app developer here: [Transmit 5](https://panic.com/transmit/).

1. Once the app is downloaded and installed properly on your computer, you should see a starter module.
2. Make sure the 'Protocol' field is set to 'SFTP.'
3. Fill in the SFTP credentials (address, username, port, and password) on the available fields:
4. Once done, click **Connect**.

## Cyberduck

Cyberduck is available both on macOS and Windows. You can download the software/app from their website: [cyberduck.io](https://cyberduck.io/)

1. After installing, you will see a starting module.
2. Click the "**Open Connection**" button on the top left.
3. You should see the login popup that you can fill in with your SFTP credentials.
4. Click the dropdown arrow next to the 'FTP (File Transfer Protocol)' option.
5. Then choose the 'SFTP (SSH File Transfer Protocol)' option.
6. Once you have done so, you should see the 'Port' area changed to `22`. Fill the fields with the credentials available under the *Settings → SFTP/SSH* tab after selecting your site [from the Sites dashboard](https://wordpress.com/sites).
7. Click **Connect**.