# Secure File Transfer Protocol (SFTP)

Secure File Transfer Protocol (SFTP) is a secure method to transfer files to and from your site. This guide will show you how to use SFTP on WordPress.com.

> This feature is available on sites with the [WordPress.com Business or Commerce plan](https://wordpress.com/hosting/?ref=developer-docs#pricing-grid).

## About SFTP

SFTP is a method to access the files and folders on a website via a client program such as [FileZilla](https://filezilla-project.org/) on your local computer. SFTP stands for Secure File Transfer Protocol (or SSH File Transfer Protocol). It was designed as an extension of the SSH (Secure SHell) protocol. The "secure" part is because it is run over a secure channel, in this case, [SSH](https://developer.wordpress.com/docs/developer-tools/ssh/).

SFTP is not a more secure version of FTP (File Transfer Protocol), even though they share similar names. While their application is similar, and both are possible via many of the same client programs, they each use very different underlying technologies.

While [GitHub Deployments](https://developer.wordpress.com/docs/developer-tools/github-deployments/) are generally used to deploy code updates to your site, SFTP is often used to transfer media files. SFTP is also useful for debugging issues with your site by allowing you to access the file system directly, especially if you use a [staging site](https://developer.wordpress.com/docs/developer-tools/staging-sites/).

## SFTP Documentation

For detailed information about using SFTP with WordPress.com, please refer to the following guides:

- [Find Your SFTP/SSH Credentials](02-credentials.md)
- [Set Up a Client](03-client-setup.md)
- [Frequently Asked Questions](04-faqs.md)