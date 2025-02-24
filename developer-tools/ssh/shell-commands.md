# Shell Commands

[Callout - info]
You should be careful with running commands to prevent data loss or damage your site. Make sure to only run commands when you know exactly what they will do.
[/Callout]

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