```
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"

brew cask install iterm2

brew install zsh zsh-completions

sudo sh -c "echo $(which zsh) >> /etc/shells"
chsh -s $(which zsh)
```
### for iterm2 profile
- Go to profiles -> Default -> Terminal -> Check silence bell to disable the terminal session from making any sound
- Download one of iTerm2 color schemes and then set these to your default profile colors
- Change the cursor text and cursor color to yellow make it more visible
- Change the font to 14pt Source Code Pro Lite. Source Code Pro can be downloaded using `brew tap homebrew/cask-fonts && brew cask install font-source-code-pro`

```





```