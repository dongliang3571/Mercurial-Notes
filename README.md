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
