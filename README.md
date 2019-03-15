# 💻 Mac -> Macbook -> Mackintosh -> { setup }

That's what I use on daily basis.
I used that configuration also on Ubuntu, so most important things work with Linux too.

<BR>

### 🤔 Who's this setup is for? 
For anyone who uses terminal, does backend with JVM languages (Java, Kotlin, Scala). Does some Machine Learning/Deep Learning stuff. Occasionally some frontend with Angular, ReactJS... or backend with NodeJS.

<BR>

### 🎲 Few essencial applications for productivity and convenience
- Anki - [`https://apps.ankiweb.net/`](https://apps.ankiweb.net/) - flashcards, so you remember everything!
- Evernote - [`https://evernote.com/download`](https://evernote.com/download) - for notes.
- Spotify - [`https://www.spotify.com/pl/download/mac/`](https://www.spotify.com/pl/download/mac/) - convinient store for playlists.
- Google Drive - [`https://www.google.com/drive/download/`](https://www.google.com/drive/download/) - drive for books, pdf, photos... etc.
- Docker - [`https://www.docker.com/get-started`](https://www.docker.com/get-started) 
- IntelliJ IDEA - [`https://www.jetbrains.com/idea/download`](https://www.jetbrains.com/idea/download)
- WebStorm [`https://www.jetbrains.com/webstorm/download`](https://www.jetbrains.com/webstorm/download)
- Visual Studio Code [`https://code.visualstudio.com/download`](https://code.visualstudio.com/download)
- Sublime - [`https://www.sublimetext.com/3`](https://www.sublimetext.com/3)
- Postman - [`https://www.getpostman.com/apps`](https://www.getpostman.com/apps)

<BR>

### 🚛 Chrome Plugins
- `Ad-Block` - well... you know.
- `Stylus` - to change CSS style of any website that you want. (I don't even remember how white-github looks like)
- `Google Translate` - if you're not English speaker (very helpfull)
- `Postman Interceptor` - proxy to capture HTTP or HTTPS requests.
- `OneTab` - convert with one-click all of your tabs into a list.
- `Toby` - best tab manager that I used. Searching through the stuff is very powerful and convinient. 
- `WhatFont` - fast way of knowing what font are you looking at.
- `VueJs` - for VueJS developers.
- `Augury` - for Angular developers
- `EmojiOne` - 🤓😎🤣

<BR>

## 🛠 Macbook Setup - Terminal
![](./images/terminal_1.png)

### ⚙ Package Manager - Brew
Brew: [`https://brew.sh/`](https://brew.sh/) <br>
Install : `/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"` <br>

### ⚙ Iterm 2 - much better terminal
Download and Install: [`https://iterm2.com/`](https://iterm2.com/) <br>
Install Theme (Dracula) : [`https://draculatheme.com/iterm/`](https://draculatheme.com/iterm/)

### ⚙ Shell for terminal 
Fish has more out-of-box, but ZSH is a bit better, more things can be customized. <br>
I have sentiment for Fish because it was first thing that I used. <br>
Either way we gonna use ZSH. <br>

ZSH: [`https://ohmyz.sh/`](https://ohmyz.sh/) <br>
Install : `sh -c "$(curl -fsSL https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"` <br>

FISH: [`https://fishshell.com/`](https://fishshell.com/) <br>
Install : `brew install fish` <br>

### ⚙ Make ZSH shell even cooler! ⚡⚡
1. In home catalog `cd ~` you should have `.zshrc` file. Open that `nano ~/.zshrc` and read it. Next install powerlevel9k.
[`https://github.com/bhilburn/powerlevel9k`](https://github.com/bhilburn/powerlevel9k) <br>
* Install: `git clone https://github.com/bhilburn/powerlevel9k.git ~/.oh-my-zsh/custom/themes/powerlevel9k` <br>
* Install & Set: [`nerd-fonts/hack/regular/complete`](https://github.com/ryanoasis/nerd-fonts/blob/master/patched-fonts/Hack/Regular/complete/Hack%20Regular%20Nerd%20Font%20Complete.ttf)
* Install those
```bash
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
git clone https://github.com/zsh-users/zsh-autosuggestions $ZSH_CUSTOM/plugins/zsh-autosuggestions
```

### ⚙ Few upgrades to common commands:

#### ⚙ Better curl (httpie)
* `brew install httpie`

![](./images/httpie.png)

### ⚙ Better `bat` 🦇 than `cat` 😾
* `brew install bat`

![](./images/bat.png)

### ⚙ Better ls (exa)
* `brew install exa`

![](./images/exa.png)

Put configuration in `~/.zshrc`  file. Open with `nano ~/.zshrc` or `vim ~/.zshrc`.
```bash
export PATH=$HOME/bin:/usr/local/bin:$PATH
export ZSH="/Users/$USERNAME/.oh-my-zsh"

ZSH_THEME="powerlevel9k/powerlevel9k"

POWERLEVEL9K_MODE="nerdfont-complete"
POWERLEVEL9K_DISABLE_RPROMPT=true
POWERLEVEL9K_PROMPT_ON_NEWLINE=true
POWERLEVEL9K_MULTILINE_LAST_PROMPT_PREFIX="┗━🎲 "
POWERLEVEL9K_MULTILINE_FIRST_PROMPT_PREFIX="┏━"

POWERLEVEL9K_SHORTEN_DIR_LENGTH=1
POWERLEVEL9K_SHORTEN_DELIMITER=""
POWERLEVEL9K_SHORTEN_STRATEGY="truncate_from_right"

POWERLEVEL9K_LEFT_PROMPT_ELEMENTS=(user dir vcs)

plugins=(
  git
  zsh-syntax-highlighting
  zsh-autosuggestions
)

# JDK
alias setJdk8='export JAVA_HOME=$(/usr/libexec/java_home -v 1.8)'
alias setJdk11='export JAVA_HOME=$(/usr/libexec/java_home -v 11)'

# exa (better ls)
alias e='exa -all'
alias ee='exa --long --header'

source $ZSH/oh-my-zsh.sh
```
## Cool features included:
- Switching easily between Java JDKs just write `setJdk8, setJdk11` to set your Java version.


<br>
<br>

## 🛠 Macbook Setup - most needed tools

### ⚙ JDK <br>
1. `brew update`
2. `brew tap caskroom/versions`
3. `brew cask install java`
4. `java -version` - to see what version of JDK you installed.
5. ```export JAVA_HOME="`/usr/libexec/java_home -v 1.8`"``` or `-v 11` depends on version you installed or use.
6. If you need install Java8 `brew tap caskroom/versions` and `brew cask install java8`
7. In `.zshrc` file you have aliases to switch between versions easily (just write setJdk8 in terminal).
(TIP re-load zsh typing `zsh` in your terminal or `source $ZSH/oh-my-zsh.sh`)

### ⚙ IntelliJ Idea - Setup 
[x] `Enable Annotation Processing` - set it as default (not only for specific project). <br> 
[x] `Create directories for empty content roots automatically` - depends if you want this to be automatic. <br>
1. Install `Lombok` and `Kotlin` plugin.
2. Install `Spock Framework Enchancements` plugin - Spock live-templates. Example use: `spgwt`
3. Install [iterm-plugin](https://plugins.jetbrains.com/plugin/10344-iterm-plugin). Open iterm from project path.
4. Create launcher script to open IDE from terminal.
Menu: `Tools -> CreateCommandLineLauncher` <br> 
From terminal: `idea .` inside of project. `idea /project` or just choose project to open.

### ⚙ Git
1. ` brew install git`
2. `git config --global user.name "your_name"`
3. `git config --global user.email "your_email@youremail.com"`

### Frontend (Angular, Node)
#### Visual Studio Code - plugins to install
* Save Typing
* IDE JetBrains Keymap
* Atom One Dark
* Auto Rename Tag
* Auto Close Tag
* Paste and indent
* Bracket Pair Colorizer
* Trailing spaces

#### Update npm: 
* `npm install -g npm`
#### Update AngularCLI: 
* `npm uninstall -g angular-cli @angular/cli`
* <del>`npm cache clean`</del> `npm cache verify`
* `npm install -g @angular/cli`
#### Sample Angular project: 
* `ng new first-frontend-app` - create project
* `yarn start` - start project
#### Install Node: 
* `brew install node`
* `npm update`
* `npm install -g node-gyp`


#### Can't build or run the project? Try these: 
* TIP-1: `ng update --all` - but be careful with that (good for new projects) 
