# Andrew's dotfiles.

[mathias's readme](https://github.com/mathiasbynens/dotfiles/) is awesome. go read it.

This repo is mostly for me but you're welcome to make suggestions.

## install the neccessary apps

```
Required Software:
* Git
* oh-my-zsh
* sass
* subl mapping
* NVM
* Node
* node-debug
* vim
* docker
* grunt
* gsutil
* gcloud
```

My basic setup is captured in `install-deps.sh` which adds homebrew, z, nvm, etc.
I will be updating this to remove nave and install oh-my-zsh

## private config

Toss it into a file called `.extra` which you do not commit to this repo and just keep in your `~/`

I do something nice with my `PATH` there:

```shell
# PATH like a bawss
      PATH=/opt/local/bin
PATH=$PATH:/opt/local/sbin
PATH=$PATH:/bin
PATH=$PATH:~/.rvm/bin
PATH=$PATH:~/code/git-friendly
# ...

export PATH
```

## Syntax highlighting

…is really important. even for these files.

Install [Dotfiles Syntax Highlighting](https://github.com/mattbanks/dotfiles-syntax-highlighting-st2) via [Sublime Text 2 Package Control](http://wbond.net/sublime_packages/package_control)


### Sensible OS X defaults

When setting up a new Mac, you may want to set some sensible OS X defaults:

```bash
./.osx
```

## Similar projects

I recommend getting a [`.jshintrc`](https://github.com/jshint/node-jshint/blob/master/.jshintrc) and [`.editorconfig`](http://editorconfig.org/) defined for all your projects.





## overview of files

####  Automatic config
* `.vimrc`, `.vim` - vim config, obv.

#### shell environement
* `.aliases`
* `.bash_profile`
* `.bash_prompt`
* `.bashrc`
* `.exports`
* `.functions`
* `.extra` - not included, explained above

#### manual run
* `install-deps.sh` - random apps i need installed
* `.osx` - run on a fresh osx machine
* `.brew` - homebrew intialization

#### git, brah
* `.git`
* `.gitattributes`
* `.gitconfig`
* `.gitignore`

* `.inputrc` - config for bash readline


## Installation

```bash
git clone https://github.com/amaxwell01/dotfiles.git && cd dotfiles && node sync.js add force
```

To update later on, just run the sync again.



```
# Create a script which connects to Github, clones the repo to the server or machine
# Then updates the contents of that repo and maps it on the machine


# Aliases
alias chef='/var/chef-solo/scripts/run_chef.sh -o -v'

# Restart bash
source ~/.bashrc


# Set variables
CONFIG=~/.bashrc
