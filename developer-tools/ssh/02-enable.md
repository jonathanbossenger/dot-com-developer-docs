## Enable SSH

If you are accessing SSH for the first time, you must create your credentials and enable SSH Access:

1. Visit your site's dashboard and navigate to the site’s *Settings* page. This may be slightly different depending on your chosen Admin Interface Style.
   1. If you’re using the Classic style: *Hosting → Site Settings*
   2. If you’re using the Default style: *Settings → Server Settings*
2. Click on the **SFTP/SSH** tab.

![01-create-credentials 1.png](images/01-create-credentials%201.png)

3. Click "**Create credentials**". This only needs to be done once and will generate the SSH username and password for the selected site. The credentials will be used for both SFTP and SSH connections.
4. If you’ve already created the credentials before, they will be displayed, but you'll need to use the "**Reset password"** button to generate a new one.

![02-enable-ssh 1.png](images/02-enable-ssh%201.png)

5. Store the password in a safe place. If you lose or forget your password, the "**Reset** **password**" button can be used to generate a new one.
6. Below the password, locate "**SSH Access"** and toggle the "**Enable SSH access to this site"** option.
7. Once SSH Access has been enabled, a connection command will appear. You can copy this command and paste it into your terminal application to connect to your server via SSH.

![03-ssh-enabled 1.png](images/03-ssh-enabled%201.png)

For more details on how to use this command to access your site via SSH, jump to the Connect to SSH instructions.

## Reset a SSH Password

If you forget or lose your SFTP/SSH password, you can reset it by returning to the *Server Settings* tab after selecting your site from the Sites dashboard.

In the SFTP/SSH credentials section, click **Reset password**.

![04-reset-password 1.png](images/04-reset-password%201.png)
