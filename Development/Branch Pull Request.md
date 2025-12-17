# (Draft) Overview of Pull Requests in Git

A pull request (often referred to as “PR”) is a proposal to merge a set of changes from one branch into a target branch.  This is usually done to [merge changes from your feature branch](Branch%20Naming%20Conventions.md) into your `main` branch. 

By creating a pull request — you are asking others to review your changes with the goal of getting your changes merged into the target branch. Pull requests provide a visual representation of the differences in the content between the source branch and the target branch. This is what enables you to review the changes before accepting them and pulling them into the target branch.

## Create Pull Request

You can create a pull request on GitHub.com with [GitHub Desktop](https://github.com/apps/desktop), [GitHub Codespaces](https://github.com/features/codespaces), on [GitHub Mobile](https://github.com/mobile), and when using the [GitHub CLI](https://cli.github.com/).

## Post Pull Request Merged

You will need to manually delete your feature branch after your changes are merged into the target branch, which is usually the `main` branch. 

### Step 1: Update your Local `main` Branch

First, you need to switch to your local `main` branch and pull the latest changes from the remote repository. The merged changes from the feature branch are now part of the remote `main` branch's history.

1. **Switch to the `main` branch**:
   
   `git checkout main`
   
1. Pull the latest changes:
   
   `git pull origin main`
   
   This command fetches the latest commits from the remote `origin` and merges them into your local `main` branch, making your local version current.

### Step 2: Delete the Feature Branch

Once your local `main` branch is updated, you can safely delete both the local and the remote feature branch.

1. Delete the local feature branch
	- Use the `git branch -d` command. The `-d` (delete) flag is a safe operation that only deletes the branch if it has been fully merged into its upstream branch (in this case, `main`).
	  
	  `git branch -d <feature-branch-name>`
	  
	- If the branch has unmerged changes and you want to delete it anyway (be careful, this discards unmerged work), use the force delete flag `-D` (capital D).
	  
	  `git branch -D <feature-branch-name>`
   
2. Delete the remote feature branch:
	- To remove the branch from the GitHub repository, use `git push` with the `--delete` flag:
	  
	  `git push origin --delete <feature-branch-name>`
	  
	- Alternatively, a shorter syntax also works:
	  
	  `git push origin :<feature-branch-name>`
	  

#### Clean Up Automatically

To streamline this process in the future — you can set a Git config value to automatically prune remote-tracking references that no longer exist on the remote when you fetch.

``` bash
git config --global fetch.prune true
```

After this setting is enabled, running `git fetch origin` will also remove any local references to branches that have been deleted on GitHub.


## Branch Creation Methods

* [Branch Pull Request in Visual Studio 2026](Branch%20Pull%20Request%20in%20Visual%20Studio%202026.md)

## Online Resources

These are additional resource that you can reference to learn more about this topic:

- Kedasha Kerr, "Beginner’s guide to GitHub: Creating a pull request", August 12, 2024, https://github.blog/developer-skills/github/beginners-guide-to-github-creating-a-pull-request/.

