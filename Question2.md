# 2. How to set multiple remote repositories for the same project? Explain the use case.

Git allows to set multiple remote repositories for different functionalities they could be set following the steps below:

**Usecase:**

1. Multiple remote repositories from either single or multiple remote providers

2. Enhanced Collaboration on different platforms

3. Maintaining multiple backups on different remote servers

**Steps:**


1. **Add a primary remote repository.**

Primary remote repository could be configured with the following command.

```
git remote add origin https://github.com/CodeWithKrushnal/Git_Assignment.git
```
2. **Verify the configuration**

Primary repo config could be verified with following command

```
git remote -v
```
3. **Add a second remote repository.**

```
git remote add gitlab https://gitlab.com/krushnal.patil/Git_Assignment.git
```
4. **Verify the Configuration**

The configuration should be similar to the following response:

```
D:\Git_Assignment git:[main]
git remote -v
gitlab  https://gitlab.com/krushnal.patil/Git_Assignment.git (fetch)
gitlab  https://gitlab.com/krushnal.patil/Git_Assignment.git (push)
origin  git@github.com-codewithkrushnal:CodeWithKrushnal/Git_Assignment.git (fetch)
origin  git@github.com-codewithkrushnal:CodeWithKrushnal/Git_Assignment.git (push)
```

1. **Github Remote (****[https://github.com/CodeWithKrushnal/Git_Assignment.git](https://github.com/CodeWithKrushnal/Git_Assignment.git)****)**

![Enter image alt description](Images/dnQ_Image_4.png)

2. **GitLab Remote (****[https://gitlab.com/krushnal.patil/Git_Assignment.git](https://gitlab.com/krushnal.patil/Git_Assignment.git)****)**

![Enter image alt description](Images/IkY_Image_5.png)