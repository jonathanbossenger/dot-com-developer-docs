# Frequently Asked Questions

## I uploaded a plugin/theme and can't see it in my dashboard?

Make sure you've uploaded it to the correct folder. If plugins aren't in `/wp-content/plugins/` and themes aren't in `/wp-content/themes/`, they won't work.

## I have modified my theme files, but my changes disappeared after the theme was updated.

This is expected if you have not used a [child theme](https://wordpress.com/support/themes/child-themes/) to make modifications, as any modifications will be overwritten by the new version of the theme. Please follow these instructions if you want to [run your own customized themes](https://wordpress.com/support/themes/child-themes/).

## I've added my site to my SFTP client, and it's not working!

Make sure you've specified an SFTP connection in your client's settings. If you use the quickconnect, make sure you prefix your SFTP address with `sftp://`.

## I uploaded images/videos via SFTP, but they are not showing in my Media Library.

This is expected as WordPress does not recognize media files uploaded via SFTP. While they are accessible via the direct URL, these will not show inside the admin area. You can use plugins like [Media Sync to resolve this, so images and videos](https://wordpress.com/plugins/media-sync/) uploaded to the site via SFTP will appear normally in your *Media*.

## What file permissions should I set?

By default, your folders and file permissions should be set to 755. Changing these settings can break your site. You'll also see some [symlinked files](https://wordpress.com/support/symlinked-files-and-folders/) may appear to have different permissions. This is normal and cannot be changed.

## Can I edit my site's wp-config.php file?

Yes, you can modify your site's `wp-config.php` file. We recommend that you do not touch this file unless absolutely necessary. If you're not sure if you should make changes, [contact us](https://developer.wordpress.com/docs/support/) before you make a change.

## Can I edit functions.php?

For most WordPress.com-provided themes, the functions.php file is [symlinked](https://wordpress.com/support/symlinked-files-and-folders/) and protected. This means it cannot be edited. However, third-party and manually installed themes allow their functions.php to be changed.

Please keep in mind that editing or adding untested code to functions.php can crash your site, and changes are often lost when the theme is updated. We recommend using plugins such as [Code Snippets](https://wordpress.com/plugins/code-snippets/) if you want to apply any modifications to your site's functions.php file. This plugin allows more control and granularity over where these snippets are run, and snippets in the plugin can be easily disabled if something does not go as expected.

## Does content uploaded via SFTP count against my site's storage limits?

Yes, the content you upload via SFTP counts against your site's [storage limits](https://developer.wordpress.com/docs/platform-features/storage/), similar to the content you upload via the [Media Library](https://wordpress.com/support/media/).

## Can I edit core WordPress files?

No, you cannot edit core WordPress files or the default WordPress.com themes and plugins. These files are essential to keep your site functional. They are not editable via SFTP.

## I uploaded a plugin using SFTP, but I can't activate it. What should I do?

While we try to ensure your site here at WordPress.com is compatible with as many plugins as possible, we've found that some plugins aren't a good fit on our platform or are otherwise incompatible. Please make sure you haven't uploaded an [incompatible plugin](https://wordpress.com/support/plugins/incompatible-plugins/).

## I'm trying to upload a theme to my site, but it says it is too big. Can I upload it via SFTP?

Yes. While you'll be able to [upload a theme](https://wordpress.com/support/themes/uploading-setting-up-custom-themes/) by going to *Appearance → Themes → Add New*, there's a 50MB upload limit for security, as some themes may include other files that are not part of the theme itself.

The first step in these cases would be to double-check if you have the correct theme files. Themes from third-party vendors may include things inside their zip file, like demo content or license information. You'll want to make sure you only upload the WordPress-installable theme files to your site.

If you've removed the extra files, but you're still getting an error, you can use SFTP to add this theme to your site by unzipping it and placing it under the `/wp-content/themes/` directory.

## Can I add custom PHP modules like ioncube?

No. While some plugins require custom PHP modules to be installed to function, this is set on the server side and cannot be changed. You can review our [server environment details here](https://wordpress.com/support/php-environment/).

## Why can't I access certain folders via SFTP?

Some directories of your file system structure are locked and cannot be accessed via SFTP. This is vital for security and helps ensure the functionality of your site.

The screenshot below shows that some core directories have a ? mark icon next to them. This denotes that the directory is part of your site's core WordPress installation. These core files cannot be modified as they are required to ensure your site is functional. 

![WordPress file structure with locked folders](https://wpdeveloperstaging.files.wordpress.com/2024/02/sftp-folders-wordpress.png)

## How do I grant my plugin or theme developer access to my site via SFTP?

If a plugin or theme developer requests access via SFTP, you can provide your SFTP credentials. It is limited to one SFTP user per site. When they no longer require access, make sure to [reset the SFTP password](credentials.md).

## What if something else goes wrong?

If something unwanted happens to your site as a result of actions in SFTP, you can [restore a previous backup of your site](https://developer.wordpress.com/docs/platform-features/real-time-backup-restore/).
