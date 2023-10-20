# OH NO, git doesn't work

So suddenly git doesn't work or you are getting this error,
```
fatal: not a git repository (or any parent up to mount point /)
Stopping at filesystem boundary (GIT_DISCOVERY_ACROSS_FILESYSTEM not set).
```

What has happened is that you have deleted a directory called `.git`. This guide should help you fix that but next time it is important to double-check what you `rm`. 

## Instructions
- In your codespaces terminal, enter the `git init` command
    - You have made a new git repository that we will connect back to the old one
- Next, you need to do at least one commit, so follow these commands:
```
git add .

git commit -m "init"
```
- After that Git needs your GitHub repository link _(the place where you open your codespace from)_ to connect to the new Git we just made. Run `git remote add origin <GitHub repo URL>` in your codespaces terminal _(remember to replace <URL> with YOUR url)_
- Finally you can sync your local Git and GitHub by running this command:

`git pull --rebase origin main`

- One last thing, new that you have saved your changes you need to push, HOWEVER this first push you need to use the special command below:

`git push --set-upstream origin main`

- Now you can push as normal

## P.S.
Git is a nifty tool and I highly recommend learning how it works on the inside and today you got just a lil taste.
