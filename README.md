# dotfiles
Dotfiles and personal preferences

## t() Function for Tree-like Directory Listing
Overview
The t() function is a custom Bash function that provides a tree-like listing of files and directories. It offers a lightweight alternative to the tree command, allowing for easy customization and integration directly into your shell environment.

### Explanation
Parameters
- $1: Specifies the directory to list (default: current directory .)
- $2: Specifies the maximum depth of the listing (default: 3 levels)

### Command Breakdown
- find -E: Finds files and directories, with -E enabling extended regex
- -maxdepth: Limits the search to a specified number of directory levels
- -not -regex: Excludes certain directories or files from the output (e.g., .git, .venv)
- sort: Sorts the output
- sed: Formats the output to create a tree-like structure

### Usage
1. Add the function to your .bash_profile or .bashrc file.
2. Run source ~/.bash_profile or source ~/.bashrc to make it available in your current session.
3. Use the function in your terminal:
```
t . 2
```
This command lists the current directory structure up to 2 levels deep.

### Customization
You can easily modify the function to exclude different directories or adjust the default depth by editing the function definition.

### Benefits
Lightweight alternative to the tree command
Customizable directly in your shell environment
Excludes common unnecessary directories by default
Feel free to contribute or suggest improvements to this function!
