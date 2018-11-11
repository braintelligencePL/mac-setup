# 💻 Mac -> Macbook -> Mackintosh -> { setup }

<BR>

### 🤔 Who this setup is for? 
For anyone who uses terminal. Meaning for everyone!

<BR>

### 🎲 Few applications for productivity and convenience
- Anki - [`https://apps.ankiweb.net/`](https://apps.ankiweb.net/) - flashcards, so you remember everything!
- Evernote - [`https://evernote.com/download`](https://evernote.com/download) - for notes.
- Spotify - [`https://www.spotify.com/pl/download/mac/`](https://www.spotify.com/pl/download/mac/) - convinient store for playlists.
- Google Drive - [`https://www.google.com/drive/download/`](https://www.google.com/drive/download/) - drive for books, pdf, photos... etc.
- Docker - [`https://www.docker.com/get-started`](https://www.docker.com/get-started) 
- IntelliJ IDEA - [`https://www.jetbrains.com/idea/download`](https://www.jetbrains.com/idea/download)
- WebStorm [`https://www.jetbrains.com/webstorm/download`](https://www.jetbrains.com/webstorm/download)
- Sublime - [`https://www.sublimetext.com/3`](https://www.sublimetext.com/3)
- Postman - [`https://www.getpostman.com/apps`](https://www.getpostman.com/apps)

<BR>

### 🚛 Chrome Plugins
- `Ad-Block` - well... you know.
- `Stylus` - to change CSS style of any website that you want. (I don't even remember how white-github looks like)
- `Google Translate` - if you're not English speaker (very helpfull)
- `Postman Interceptor` - proxy to capture HTTP or HTTPS requests.
- `OneTab` - convert with one-click all of your tabs into a list.
- `WhatFont` - fast way of knowing what font are you looking at.
- `VueJs` - for VueJS developers.
- `EmojiOne` - 🤓😎🤣

<BR>

## 🛠 Macbook Setup

### ⚙ Package Manager - Brew
Brew: [`https://brew.sh/`](https://brew.sh/) <br>
Install : `/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"` <br>

### ⚙ Iterm 2 - much better terminal
Download: [`https://iterm2.com/`](https://iterm2.com/)

### ⚙ Shell for terminal 


Fish has more out-of-box, but ZSH is a bit better, more things can be customized. 
I have sentiment for Fish because it was first thing that I used.
FOR YOU BETTER CHOICE IS ZSH (probably).

ZSH: [`https://ohmyz.sh/`](https://ohmyz.sh/) <br>
Install : `sh -c "$(curl -fsSL https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"` <br>

FISH: [`https://fishshell.com/`](https://fishshell.com/) <br>
Install : `brew install fish` <br>
<br>

### Even cooler ZSH Shell!
1. In home catalog `cd ~` you should have `.zshrc` file. Open that `nano ~/.zshrc` and read it.

2. Get powerlevel9k and set it inside of `nano ~/.zshrc` file. <br>
[`https://github.com/bhilburn/powerlevel9k`](https://github.com/bhilburn/powerlevel9k) <br>
* Install: `git clone https://github.com/bhilburn/powerlevel9k.git ~/.oh-my-zsh/custom/themes/powerlevel9k` <br>
* Set: `ZSH_THEME="powerlevel9k/powerlevel9k"` <br>



### Configuration of ZSH

### ⚙ JDK <br>
1. `brew update`
2. `brew tap caskroom/versions`
3. `brew cask install java`
4. `java -version` - to see what version of JDK you installed.
5. ```export JAVA_HOME="`/usr/libexec/java_home -v 1.8`"``` or `-v 11` depends on version you installed or use.

### ⚙ IntelliJ Idea - Setup 
1. [x] Enable Annotation Processing
2. Install `Lombok` plugin (even if you not use it. You'll eventually encounter project where it is used)

### Git
1. ` brew install git`
2. `git config --global user.name "your_name"`
3. `git config --global user.email "your_email@youremail.com"`




