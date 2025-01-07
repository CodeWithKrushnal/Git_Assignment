# 5. Why is it not possible to create two branches with the names fix and  fix/bug in a Git repository, and what causes this conflict?

In Git, it is not possible to create two branches with names such as **fix** and **fix/bug **simultaneously because of how Git handles branch names and directory structure. This behavior arises due to the conflict between the naming conventions used for branches and file paths in Git.

Error Message:

```
krush@Ultron MINGW64 /d/conflict-demo (master)
$ git branch bug/fix
fatal: cannot lock ref 'refs/heads/bug/fix': 'refs/heads/bug' exists; cannot create 'refs/heads/bug/fix'
```
Resolution:

1. Use Unique Naming

2. Rename Existing Branches

3. Delete Conflicting Branch
