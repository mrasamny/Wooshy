# Introduction to GitHub for Project Collaborators
#### Uses workshop material created by Kyle Gavin

## Overview
This repository hosts a repository for a Greenfoot group project focusing on basic GitHub operations from a **group perspective**. In this workshop we will be operating in teams to explore concepts like commits, pushing, branching, pull requests, merge conflicts, and collaboration best practices.

The repository consists of Greenfoot files, including a greenfoot.jar file that contains all the Greenfoot classes. 
This tutorial will use the IntelliJ IDE by JetBrains to manage Git and GitHub tasks.  NOTE: the greenfoot.jar file
is included so that IntelliJ does not complain about undefined classes like World and Actor.

**Your group has been added as collaborators to your workshop project repo**

## Task 1 - Forking the repository and adding collaborators

Your instructor should have provided a link on Blackboard for the Wooshy repo.  Only one member of the
team should fork that repository.

Once the repository is forked, the group member should add all team members as collaborators to the repo with
**write privileges**.

Team members should look in their emails for an invitation and accept the invitation.

## Task 2 - Cloning Your Repo

In IntelliJ, clone the repo by using the HTTPS URLs provided on Blackboard.

## Task 3 - Divide and Conquer - Feature Branching

A commit is a record or bookmark representing some change (addition or deletion) of code. Generally, commits should be small changes. Commits are local changes, that can be reversed. 
A collection of commits that is working as intended can be pushed (sent to the remote repository as an official change).

Prior to starting work on a new feature, make a pull request from the main branch.  This synchronizes the 
main branch on GitHub with the local main branch on your computer.

Let's assume that each member will be creating their own actor for the game.  
Each group member creates a new branch from the main branch. 
The name of the branch should reflect the feature that you are adding. So, if I am adding a start button
to the game, I would call the new branch **marwan_start_button**.

Remember to "Checkout" your branch. When you checkout a branch, all your local commits will be sent to 
that respective branch, and your pushes will be sent to the remote branch. 
When you've checked out the new branch, subclass Actor in Greenfoot and give the class a name.

Now, commit and push your changes in your feature branch. 
Then, create a pull request and merge your changes to the main branch. 
Notice that since we are modifying separate files through this branching process, 
there is no merge conflict.

## Task 4 - Dealing With Conflicts

As a team, you need to make sure that you communicate and collaborate in such a way that major conflicts
do not occur when you merge new features into the main branch.  Conflicts will occur when more than
one team member makes changes to the same file.  Major conflicts occur when more than one member makes
changes to the same part of a file.  Major conflicts are avoided if one team member takes ownership of
changes to a specific file.

Before you begin, make sure to create a new feature branch and checkout or switch to the new branch.

Let's simulate a conflict, by modifying the MyWorld class.  Add a method as follows:

```java
public void add<MyObject>(){
    java.util.Random rand = new java.util.Random();
    addObject(new <MyObject>,rand.nextInt(getWidth()),rand.nextInt(getHeight()));
}
```

Once this is added with no syntax errors, you will need to make sure that you add a call to `add<MyObject>` 
from within the `MyWorld` constructor.

Test that your object is randomly placed on the world each time you press reset.  Once this is working
as expected, head over to IntelliJ.  Commit and push the changes on your feature branch.  Go to your repo
on GitHub and do a pull request to merge your new feature to the main branch.  Have one member responsible
carry out the pull and resolve the conflicts.


## Summary and Conclusion

In this workshop, you learned how to
- [X] Clone your group project.
- [X] Add a feature branch to your local project, push the changes, and do a pull request.
- [X] Deal with pull conflicts and how to resolve conflicts. 
