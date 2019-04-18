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

### do stuff in a sub repo

```bash
hg -R <subrepo> <commands>
```

### check identity the working directory or specified revision

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
