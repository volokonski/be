# Git Notes

### How to config Git

```
git config --global user.name "User Name"
git config --global user.email user@email.com
ssh-keygen -t rsa -b 4096
cat ~/.ssh/id_rsa.pub
```

> Find out How to connect GitHub with SSH here:
> https://docs.github.com/en/authentication/connecting-to-github-with-ssh

**Please note:** you can have your own extra local\corporate configs for any directory (nested):

1. Let's check our home git config: `cd ~; cat .gitconfig`
1. Now we create new repository: `mkdir work-folder; cd work-folder; git init; ls -a`
1. Let's copy here our global git config file from home directory: `cp ~/.gitconfig ~/work-folder/; ls -al; cat .gitconfig`
1. And change the credits: `vi .gitconfig`

   ```
   i - edit mode
   escape - command mode
   yy - copy line
   p - paste line
   ctrl+u ctrl+d - scroll
   :w - save
   :q - quit
   :wq - save and quit

   /of - finds "of"
   press <n> key to find next
   ```

1. Cool, now let's delete this whole _work_ folder: `rm -r ~/work-folder`

### [Optional] How to create main repository locally

```
git init
git branch -m main
cat > README.md
git add -A
git commit -m "init commit"
git remote add origin git@github.com:USER/REPO.git
git log
git log --oneline
```

### How to clone and check repository

```
git clone *your_repo_link*
git status
git branch
```

### To upload, save on local stage env, commit & push

```
git add -A
git commit -m 'add comment text'
git push origin <branch_name>
```

### Change your branch / create a new one and move into it

```
git checkout fix1
git checkout -b fix2
```

### Work with tags (use after commit, better to push after the merge/release)

```
git tag v.0.0.1
git tag v.0.0.2
git tag
git push origin v.0.0.2
```

To push all tags: `git push origin --tag`

### [Optional] Merge data locally between two branches

```
git checkout main
git merge fix-readme
```

### Run the git cherry pick command to merge the commit with your branch:

```
git cherry-pick <sha1-commit-hash>
```

### Don't forget to update main branch

Before each work: `git pull origin main`

## Some links:

1. [YouTube Git Lessons by IT-INCUBATOR](https://www.youtube.com/playlist?list=PLbLBXDhswD1eq9M-KavTK98Z4OI00VbsW)
1. [Tweak zsh for Mac](https://www.themoderncoder.com/add-git-branch-information-to-your-zsh-prompt/)
1. [Gitignore](https://stackoverflow.com/questions/18393498/gitignore-all-the-ds-store-files-in-every-folder-and-subfolder)
1. [GitHub's HowTo all steps guide](https://gist.github.com/vlandham/3b2b79c40bc7353ae95a)
1. [Convention for Naming Branches](https://dev.to/varbsan/a-simplified-convention-for-naming-branches-and-commits-in-git-il4)
1. [Git merge. It is also used to merge multiple commits into one history.](https://www.w3docs.com/learn-git/git-merge.html)
1. [Squash](https://stackoverflow.com/questions/6934752/combining-multiple-commits-before-pushing-in-git)
1. [Brief helper](https://timeweb.cloud/tutorials/git/git-push-kak-rabotaet-komanda)

# See ya!
