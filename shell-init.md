### Install Homebrew and other dev apps

```
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"

brew cask install docker

brew cask install iterm2

brew install zsh zsh-completions

sudo sh -c "echo $(which zsh) >> /etc/shells"
chsh -s $(which zsh)

mkdir ~/dev
```

### Adjust iterm2 profile
- profiles -> Default -> General -> Working Driectory to choose Directory `~/dev`
- profiles -> Default -> Window -> Columns to 120, Rows to 38
- profiles -> Default -> Terminal -> Check silence bell to disable the terminal session from making any sound
- Download one of iTerm2 color schemes and then set these to your default profile colors
- Change the cursor text and cursor color to yellow make it more visible
- Change the font to 14pt Source Code Pro Lite. Source Code Pro can be downloaded using `brew tap homebrew/cask-fonts && brew cask install font-source-code-pro`

```
sh -c "$(curl -fsSL https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"

git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting

git clone https://github.com/zsh-users/zsh-autosuggestions $ZSH_CUSTOM/plugins/zsh-autosuggestions

open ~/.zshrc
  
  ZSH_THEME="agnoster"

  plugins=(
  git
  zsh-syntax-highlighting
  zsh-autosuggestions
  )
```

### nvm & node

```
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.34.0/install.sh | bash
nvm install 12

```


