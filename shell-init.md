```
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"

brew cask install iterm2

brew install zsh zsh-completions

sudo sh -c "echo $(which zsh) >> /etc/shells"
chsh -s $(which zsh)

brew tap caskroom/fonts && brew cask install font-source-code-pro

```