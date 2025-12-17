# Committing Changes in Visual Studio 2026 with Git

Visual Studio 2026 is the latest version of Visual Studio. The Git integration features for branch creation follow the same robust process as its immediate predecessors (Visual Studio 2022).

## Recommended Steps to Commit Changes

1. **Open your repository**: Ensure you have a previously created or cloned Git repository open in Visual Studio.
2. Verify that .NET solution compiles on your local machine.
3. Verify that the unit tests in the .NET solution pass.
4. **Access the "Git Changes" window**: You have two primary options:
    - **Menu Bar**: In the menu bar in the upper left-hand corner of the window — go to the "**Git**" menu and then choose the "**Commit or Stash**" option in the menu.
    - **Window Tab**: The "Git Changes" window maybe open and in a tab group already — click the tab, normally near the "Solution Explorer" tab.
- Submit "Git Changes" form
	-  **Enter a message**: In the **Git Changes** form, enter a [commit message that follows our best practices](Branch%20Commit%20Message%20Conventions.md).
	- Choose your button to submit the changes:
		- "Commit All" — commits the changes locally.  The remote repository remains unchanged.
		- "Commit All and Push" — commits the changes locally and pushes the changes to the remote repository.  The remote repository will be updated with the changes. 
		- "Commit All and Sync" —commits the changes locally, pushes the changes to the remote repository, and performs a push.  Your changes are made on the remote repository and your local repository is synced with the remote repository to get any additional changes that have been made on the remote.


