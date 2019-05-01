# Mercurial-Notes
Mercurial Commands

### Switch branch

```bash
hg update <branch-name>
```

to clean all current changes while switching branches

```bash
hg update -C|--clean <branch-name>
```

update to a specific revision

```bash
hg update -r|--rev <revision>
```

### Show branch name

current branch name

```bash
hg branch
```

list all branches

```bash
hg branches

# show closed branches too
hg branches -c|--closed
```

### Close a branch

```bash
hg commit --close-branch
```

### Create a branch

```bash
hg branch <branch-name>
```

### Push new branch to remote

```bash
hg push -b <branch-name> --new-branch
```

### revert changesets without removing commits

```bash
hg revert --all -r <parent of rev-to-revert>
```

### revert by creating a new head

```bash
hg update -r <rev-to-revert>
# this is similar to git checkout <commit-hash>
```

### Check logs

all logs from all branches

```bash
hg log
```

logs for a specified branch

```bash
hg log -b <branch-name>
```

limit number of logs to be displayed

```bash
hg log -b <branch-name> -l <a-number>
```

### Do stuff in a sub repo

```bash
hg -R <subrepo> <commands>
```

### Check identity the working directory or specified revision

current directory with current revision

```bash
hg id

# output: f8df3081b002 (BETA) tip
```

current directory with a specific revision 

```bash
hg id -r|--rev <revision>
```

a subrepo directory with current revision

```bash
hg -R <subrepo> id
```

get a complete id that is stored in .hgsubstate

```bash
hg --debug id

# output: d5ab68e45277f9134562a780a2d0ccc3e07e15ac (Wanaka_EU_Common)
```
