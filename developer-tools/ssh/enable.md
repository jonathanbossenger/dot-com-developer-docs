# Enable SSH Access

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

![The SFTP/SSH credentials section within the WordPress.com Hosting Configuration page with an orange arrow pointing to SSH Access](../images/ssh-access-toggle.png)

6. Once SSH Access has been enabled, a connection command will appear. This can be copied and pasted into a terminal application. Review our Connect to SSH instructions for more on accessing your site via SSH.

![Activated SSH Access toggle displaying sample command: ssh example.wordpress.com@sftp.wp.com](../images/ssh-command-example.png)

## Reset a SSH Password

If you forget or lose your SFTP/SSH password, you can reset it by returning to "**Server Settings**" tab after selecting your site from the Sites dashboard.

Within the SFTP/SSH credentials section, click **Reset password**. 