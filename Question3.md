# 3. What happens when a file is deleted in the main branch and updated in a feature branch, and how is this handled during a merge?

When a file is **deleted** in the **main** branch and **updated** in a **feature** branch, a merge conflict occurs during the merge process because Git identifies this as a conflicting change. This conflict needs to be resolved manually, as Git cannot automatically decide whether to delete the file or keep the updated version.

**Conflict Message:**

```
krush@Ultron MINGW64 /d/conflict-demo (master)
$ git merge feature-branch
CONFLICT (modify/delete): file.txt deleted in HEAD and modified in feature-branch.  Version feature-branch of file.txt left in tree.
Automatic merge failed; fix conflicts and then commit the result.
```
Resolution could be Could be done with either by adding or deleting the disputed file.
