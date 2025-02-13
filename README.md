# dotfiles
Dotfiles and personal preferences

The t() function you are referring to is a custom Bash function that can be defined to list files and directories in a tree-like format. While I cannot provide direct links, I can summarize the relevant information based on the search results.
The function can be implemented as follows:

Explanation of the Function


Parameters:

The first parameter (\$1) specifies the directory to list. If not provided, it defaults to the current directory (.).
The second parameter (\$2) specifies the maximum depth of the listing. If not provided, it defaults to 3 levels deep.



Command Breakdown:

find -E: This command is used to find files and directories, with -E enabling extended regex.
-maxdepth: Limits the search to a specified number of directory levels.
-not -regex: Excludes certain directories or files from the output, such as .git, .venv, etc.
sort: Sorts the output.
sed: Formats the output to create a tree-like structure.



Usage
You can use this function in your terminal after defining it in your .bash_profile or .bashrc file. After adding it, run source ~/.bash_profile or source ~/.bashrc to make it available in your current session.
To list the current directory structure up to 2 levels deep, you would run:

`t . 2`

This function provides a lightweight alternative to the tree command, allowing for customization and integration directly into your shell environment.