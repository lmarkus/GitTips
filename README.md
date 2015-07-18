# GitTips
Some git shortcuts to make your life easy

## Setup

### Install git
1.- Make sure you have the latest version of git. [Download it here](http://git-scm.com/download/)

2.- Check your install: `git --version`. Usually, git will install into `/usr/local/git` however, OSX ships with it's own version of git, which can take precedence. If your git version is not what you expect, try renaming apple's version: 

```bash
sudo mv /usr/bin/git /usr/bin/git-apple
```


### Set up autocomplete for git:
1.- Save [git-completion.bash](https://raw.githubusercontent.com/git/git/master/contrib/completion/git-completion.bash) on your home directory. (I highly recommend you rename it to  `.git-completion.bash` (Note the dot at the beginning)

2.- If you're on a Mac, open your `~/.profile` file and add the following entry (For other systems use `.bashrc`):

```bash
# Run git autocomplete
source ~/.git-completion.bash
```

3.- Reload the terminal.  Test it: `git check<tab>` should autocomplete to `git checkout`

### Set up your name:

This comes in handy for identifying your commits in git's history

```bash
$ git config --global user.name "John Doe"
$ git config --global user.email johndoe@example.com
```


## Smoke and Mirrors for the presentation
- Watch: `watch  "cd gitClass/.git/objects; find ./ -type file | tr -d './'"`  This command shows all the objects in the git database. (It removes any slashes and dots, so we see the pure SHA1 checksum) *Note: Requires installing the `watch` command on Mac. Homebrew install recommended.
- Show: `alias show="git cat-file -p"` quick alias to shows the content of a git object.
