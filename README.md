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
