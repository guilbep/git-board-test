# git-board-test

A playground for [git-board](https://github.com/guilbep/git-board) and the
git-bug bridge-sync fork: 24 dummy issues, and the private Project
https://github.com/users/guilbep/projects/1, with the same fields as
EPFL-ENAC's Project 40 (status, priority, size, category, module, est.
hours, sprint). Break anything here.

```bash
git clone git@github.com:guilbep/git-board-test.git && cd git-board-test
git bug pull                      # the issues, as git-bug data
git bug user adopt 9dcbc62        # write as Guilbert Pierre (or: git bug user new)
git board                         # the terminal UI
git-board-server --addr 127.0.0.1:8080 --me guilbep   # the web UI
git-board bridge sync             # what a sync with Project 1 would change
```

`.git-board.toml` is optional: without it every `ns:value` label is a
field. Here it gives the option order (status follows the workflow), the
sprint dates behind `@current`, the views, and the Project to sync with
(`write = true`: this Project may be written to).
