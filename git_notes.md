## Add branch name to display in terminal

Open ~/.bash_profile in your favorite editor and add the following content to the bottom.

# Git branch in prompt.


```
parse_git_branch() {
  git branch 2> /dev/null | sed -e '/^[^*]/d' -e 's/* \(.*\)/ (\1)/'
}

export PS1="\u@\h \W\[\033[32m\]\$(parse_git_branch)\[\033[00m\] $ "
```

By MARTIN FITZPATRICK at [http://martinfitzpatrick.name/article/add-git-branch-name-to-terminal-prompt-mac/](http://martinfitzpatrick.name/article/add-git-branch-name-to-terminal-prompt-mac/)
