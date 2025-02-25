# Enable SSH Access

If you are accessing SSH for the first time, you must first create your SSH credentials and enable SSH Access.

## Create WordPress.com SSH Credentials

\[Callout block \- info\]

If you have already created the SSH credentials, perhaps when you set up SFTP access, you can use the same password for SSH. 

\[/Callout block\]

Visit your site's WordPress.com dashboard and navigate to Hosting → **Overview** (or Settings → **Hosting Configuration** if using the default interface style). Click the **Server Settings** tab. 

Click **Create credentials**. This only needs to be done once and will generate the SSH username and password for the selected site. These credentials are used for both SSH and [SFTP](docs.wordpress.com/developer-tools/sftp) connections. 

Store the password in a safe place, as it will only be displayed once.

### Generating a new password/Resetting the password

If you forget or lose your SFTP/SSH password, you can reset it by returning to "**Server Settings**" tab after selecting your site from the Sites dashboard.

In the SFTP/SSH credentials section, click **Reset password**.

## Enable SSH

To enable SSH access, locate **SSH Access** and toggle on the **Enable SSH access to this site** option.

![The SFTP/SSH credentials section within the WordPress.com Hosting Configuration page with an orange arrow pointing to SSH Access](../images/ssh-access-toggle.png)

Once SSH Access has been enabled, a connection command will appear. This is the command you will use in your terminal to connect to the server via SSH. 

![Activated SSH Access toggle displaying sample command: ssh example.wordpress.com@sftp.wp.com](../images/ssh-command-example.png)

See our [Connect to SSH]() instructions on how to connect to your site via SSH using this command.

