### Install Homebrew

```
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"

mkdir ~/dev
```

### go
```
brew install golang
```

### git

```
git config --global core.ignorecase false

```

### iterm2
```
brew cask install iterm2
brew tap homebrew/cask-fonts
brew install --cask font-source-code-pro
brew install --cask font-hack-nerd-font
```

- Preferences -> Appearance -> General, status bar lower.
- profiles -> Default -> General -> Working Driectory to choose Directory `~/dev`
- profiles -> Default -> Window -> Columns to 120, Rows to 38
- profiles -> Default -> Terminal -> Check silence bell to disable the terminal session from making any sound
- Download one of iTerm2 color schemes and then set these to your default profile colors
- Change the cursor text and cursor color to yellow make it more visible
- Change the font to 14pt Source Code Pro Lite.

### zsh

```
# brew install zsh
brew install zsh-completions

# sudo sh -c "echo $(which zsh) >> /etc/shells"
# chsh -s $(which zsh)

sh -c "$(curl -fsSL https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"

# reload shell

git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting

git clone https://github.com/zsh-users/zsh-autosuggestions $ZSH_CUSTOM/plugins/zsh-autosuggestions

git clone --depth=1 https://github.com/romkatv/powerlevel10k.git $ZSH_CUSTOM/themes/powerlevel10k

open ~/.zshrc

  export PATH=$HOME/bin:/usr/local/bin:$PATH

  ZSH_THEME="powerlevel10k/powerlevel10k"

  plugins=(
  git
  zsh-syntax-highlighting
  zsh-autosuggestions
  )
  
  # add this line to the end of file
  # To customize prompt, run `p10k configure` or edit ~/.p10k.zsh.
  [[ ! -f ~/.p10k.zsh ]] || source ~/.p10k.zsh
```

### node.js

```
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.38.0/install.sh | bash
nvm install 12

open ~/.zshrc
  export NVM_DIR="$HOME/.nvm"
  [ -s "$NVM_DIR/nvm.sh" ] && . "$NVM_DIR/nvm.sh" # This loads nvm

open ~/.p10k.zsh
  function prompt_example() {
    local node_ver="$(nvm current)"
    # -i '⭐'
    p10k segment -f 208 -t "node: ${node_ver[(ws:.:)1]}"
  }

```

### python3
```
brew update && brew install python

# open ~/.zshrc
#  alias python=/usr/local/bin/python3
  
```


### docker
```
brew install --cask docker

open ~/.zshrc
  docker rmi $(docker images -f "dangling=true" -q)
  
```

### java
```
brew install AdoptOpenJDK/openjdk/adoptopenjdk{11,14}

function jdk
	set java_version $argv
	set -Ux JAVA_HOME (/usr/libexec/java_home -v $java_version)
	java -version
end
```
ref to [link](https://github.com/AdoptOpenJDK/homebrew-openjdk)

### vscode

```
brew cask install visual-studio-code

# install setting sync, then sync setting from gits
https://marketplace.visualstudio.com/items?itemName=Shan.code-settings-sync
```
