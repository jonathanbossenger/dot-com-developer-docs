# SSH Keys

The instructions below will guide you through the process of adding an SSH Key to your WordPress.com account. Importantly, you'll need to first generate an SSH key, then add the SSH key to your account. Finally you'll attach the SSH key to any sites you'd like to use it with.

You can only add one key per WordPress.com account which you can then attach to multiple sites. Each site can have multiple keys attached, one per privileged user.

If you don't have an SSH Key on your computer, connecting to SSH via password authentication also works.

## Generate an SSH Key

You can generate SSH keys on Mac, Windows, and Linux. Once you create your key, you can then add your public key to your WordPress.com account.

### Create an SSH Key on MacOS and Linux

To generate an SSH key using macOS, take the following steps:

1. Open the Terminal.
2. Run the command `ssh-keygen -t rsa`.
3. When prompted, enter the name of the file where you wish to store your key or press `Enter` to accept the default file name.
4. When prompted, type a secure passphrase to use with your key.

This will save a public and a private key in the chosen location. The public key, which you'll need for your WordPress.com account in the next step, will include the .pub extension.

### Create an SSH Key on Windows

To generate an SSH key using Windows, take the following steps:

1. Open PowerShell or cmd prompt.
2. Run the command `ssh-keygen`.
3. When prompted, enter the name of the file where you wish to store your key or press `Enter` to accept the default file name.
4. When prompted, type a secure passphrase to use with your key.

This will save a public and a private key in the chosen location. The public key, which you'll need for your WordPress.com account in the next step, will include the `.pub` extension.

## Add an SSH Key to Your Account

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

![An orange arrow pointing to the SSH key checklist item under the Security Checklist on WordPress.com](../images/ssh-key-checklist.png)

4. Paste your SSH Key to the **Public SSH Key** field.

![SSH Key section showing details about the key and the SSH Public Key field](../images/ssh-key-details.png)

5. Click on the **Save SSH Key** button.

Importantly, once you add your SSH key to your WordPress.com account, you'll then need to attach it to each site you'd like to use it on.

## Attach an Existing SSH Key to a Site

After adding an SSH Key to your account, it will be necessary to attach it to the site you want to connect via SSH. To attach your SSH Key to a site, follow these steps:

1. Visit your site's dashboard and navigate to Hosting → **Overview** (or Settings → **Hosting Configuration** if using the default interface style).
2. Click the Server Settings tab.
3. Under the **SSH Access** section, use the **SSH Keys** field to select the desired key.

![SSH key username-default on WordPress.com](../images/ssh-key-username.png)

4. Click on the **Attach SSH Key** to Site button.

Once your SSH key is attached to the site, you can use the SSH key when authenticating over SSH.

## Detach a Key from a Site

If you no longer want to connect to a site using your SSH Key, you can detach the key from the site by following these instructions:

1. Visit your site's dashboard and navigate to Hosting → **Overview** (or Settings → **Hosting Configuration** if using the default interface style).
2. Click the Server Settings tab.
3. Under the **SSH Access** section, locate the SSH Key you want to remove.
4. Click on the **Detach** button to remove the key from the site.

The SSH key will still be associated with your WordPress.com account until you remove it.

## Update an Existing SSH Key

Follow the below steps to update your public SSH key:

1. From your WordPress.com dashboard, go to _My Profile_.
2. On the My Profile page, click on _Security_.
3. Click on the **SSH Key** option available in the Security Checklist.
4. Click on the **Update SSH key** button next to the key you wish to update.

![SSH key username-default on WordPress.com with two buttons - Update SSH key and Remove SSH key](../images/ssh-key-update-buttons.png)

5. Paste your updated SSH Key to the **New SSH Public Key** field.

![the Update SSH key section on WordPress.com](../images/update-ssh-key.png)

6. Click the **Update SSH Key** button to save changes.

## Remove an Existing SSH Key

Removing an SSH key from your WordPress.com account will also detach it from each site it's associated with. To remove an existing SSH Key from your WordPress.com account, follow these steps:

1. From your WordPress.com dashboard, go to My Profile.
2. On the My Profile page, click on Security.
3. Click on the **SSH Key** option available in the Security Checklist.
4. Click on the Remove SSH Key button displayed beside the existing key.
5. A confirmation message will be displayed. Confirm you want to remove the key by clicking on the OK button. 