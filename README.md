# ~/sourced/functions
Custom functions for oh-my-zsh

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

## What's inside?

* Script to create project asset directories and Sublime project files configured for MAMP environment (forked from [Brad Parbs' dotfiles](https://github.com/bradp/dotfiles)).
* Script to set up a new WordPress installation, built for MAMP + WP-CLI, specifically.
* Various helper functions associated with new site setup.
