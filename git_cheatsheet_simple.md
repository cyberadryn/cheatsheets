# Git Cheatsheet - Cloud Engineer Academy

## Initial Setup

```bash
git init                    # Initialize a new Git repository
git clone [url]            # Clone/download a repository from remote
git config --global user.name "[name]"     # Set your username
git config --global user.email "[email]"   # Set your email

```

## Basic Commands

```bash
git status                 # Check status of working directory
git add [file]            # Add a file to staging area
git add .                 # Add all changed files to staging area
git commit -m "[message]" # Commit changes with a message
git log                   # View commit history

```

## Working with Branches

```bash
git branch                # List all branches
git branch [name]        # Create a new branch
git checkout [branch]    # Switch to a branch
git checkout -b [branch] # Create and switch to a new branch
git merge [branch]       # Merge specified branch into current branch
git branch -d [branch]   # Delete a branch

```

## Remote Repository Operations

```bash
git remote add origin [url]   # Connect local repository to remote
git push origin [branch]      # Upload local branch to remote
git pull origin [branch]      # Download and merge changes from remote
git fetch                     # Download changes from remote (without merging)
git remote -v                 # List remote repositories

```

## Undoing Changes

```bash
git restore [file]           # Discard changes in working directory
git restore --staged [file]  # Unstage a file
git reset HEAD~1            # Undo last commit, keep changes
git reset --hard HEAD~1     # Undo last commit, discard changes
git revert [commit]         # Create new commit that undoes specified commit

```

## Common Workflows

### Starting a New Project

1. Initialize repository:
    
    ```bash
    git init
    git add .
    git commit -m "Initial commit"
    
    ```
    
2. Connect to remote:
    
    ```bash
    git remote add origin [url]
    git push -u origin main
    
    ```
    

### Making Changes

1. Create a feature branch:
    
    ```bash
    git checkout -b feature-name
    
    ```
    
2. Make changes and commit:
    
    ```bash
    git add .
    git commit -m "Add feature X"
    
    ```
    
3. Push changes:
    
    ```bash
    git push origin feature-name
    
    ```
    

### Updating Your Repository

1. Get latest changes:
    
    ```bash
    git pull origin main
    
    ```
    
2. Merge main into your branch:
    
    ```bash
    git checkout feature-name
    git merge main
    
    ```
    

## Best Practices

- Commit often with clear, descriptive messages
- Pull before pushing to avoid conflicts
- Create new branches for new features/fixes
- Keep commits focused and atomic
- Review changes before committing (`git diff`)
- Keep your main/master branch stable

## Common Issues and Solutions

### Merge Conflicts

When Git can't automatically merge changes:

1. Open conflicted files (marked with >>>> and <<<<)
2. Resolve conflicts manually
3. Add resolved files
4. Commit changes

### Accidentally Committed to Wrong Branch

```bash
git reset HEAD~1           # Undo commit but keep changes
git stash                  # Save changes temporarily
git checkout correct-branch
git stash pop             # Apply saved changes

```

### Need to Update Commit Message

```bash
git commit --amend -m "New message"  # Update last commit message

```

## Tips for Beginners

- Use `git status` frequently to understand repository state
- Create a `.gitignore` file for files you don't want to track
- Practice with a test repository first
- Use `git help [command]` for detailed documentation