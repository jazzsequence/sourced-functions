# ~/sourced/functions
Custom functions for oh-my-zsh

#### Version 0.9.6

### Usage
1. In your `~/.zshrc` file, make sure you have the following lines:

```
source $ZSH/oh-my-zsh.sh
for file in /Users/{your username}/sourced/*; do
        source "$file"
done
```
2. Save this file to `/Users/{your username}/sourced/`.
3. Profit!

**Note:** Also make sure you have [ZSH](http://www.zsh.org/) and [Oh My ZSH!](https://github.com/robbyrussell/oh-my-zsh) installed. That's kind of important.

**Optional**
You can also clone this repo and get updates whenever it's updated. In that case, clone it somewhere, like `~/git`:

`$ git clone git@github.com:jazzsequence/sourced-functions.git ~/git/sourced-functions`

Then create a symbolic link in your `~/sourced` folder:

`$ ln -s ~/git/sourced-functions/functions ~/sourced`

## What's inside?

* Script to create project asset directories and Sublime project files configured for MAMP environment (forked from [Brad Parbs' dotfiles](https://github.com/bradp/dotfiles)).
* Prompt-based script to set up a new WordPress installation, built for MAMP + WP-CLI or Chassis.
* Various helper functions associated with new site setup.
* A wp-cli search/replace alias (`sr`) that will prompt to change a site's URLs.
* Commands for launching/killing the Global Protect VPN client (which cannot be turned off once installed and running within the app itself).

## New site setup
The functions file includes a number of functions built for new site setup for MAMP and MAMP Pro. Usage is simple and will prompt for user input:

```
$ mkdir project-name && cd project-name
$ newsite
```

## New site setup with Chassis
The functions file also includes functions required for setting up a new site with Chassis. Required Vagrant to be installed. Simply run `newsite` and choose the Chassis option when prompted. The prompts will walk you through the rest.


## FAQ

**How come I get a database connection error when I try to set up a new site in MAMP?**
That's because WP-CLI is trying to use the version of PHP installed on your _system_ instead of the one that MAMP is using. The most reliable way to get around this that I have found (and I've tried a bunch of things) is to create a symbolic link to your MAMP `php` binary in `/usr/bin`. Like this:

```
$ sudo mv /usr/bin/php /usr/bin/php-osx # move the old php binary.
$ sudo ln -s /Applications/MAMP/bin/php/php5.6.25/bin/php /usr/bin/php # create a symbolic link to a version of PHP in MAMP.
```

Look in `/Applications/MAMP/bin/php` for your exact version of PHP -- it varies depending on what version of PHP you are running. When you upgrade your operating system, it's entirely possible that you will need to repeat this process.
