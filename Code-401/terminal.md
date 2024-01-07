# Terminal

## The Command Line

The command line, also known as a terminal, is a text-based interface for interacting with your computer's operating system. Unlike the graphical user interface (GUI) of systems like Windows and OSX, the command line relies on typed commands instead of graphical elements like buttons and icons. Users type commands into the prompt, which are then executed by the system, often resulting in text-based feedback. The command line allows for multiple instances to be open simultaneously, enabling users to perform various tasks in each. Common in Linux and macOS (and accessible in Windows through different means), it's a powerful tool that can enhance productivity and control, especially for more technical tasks. The tutorial further explains that most systems use Bash (Bourne Again SHell) as their shell, which is the program that runs in the terminal to execute commands.

## Navigation

### Understanding the Linux Directory System

Linux has a hierarchical file system with the root directory at the top, denoted as /. Files and directories reside at various levels in this hierarchy.

### Navigating Commands

- pwd (Print Working Directory): Displays your current directory.
  - Example: Running pwd might return /home/user.
- ls (List): Shows the contents of a directory.
  - Basic Usage: ls lists contents of the current directory.
  - With Options: ls -l provides a detailed listing.
  - With Path: ls /etc lists contents of the /etc directory.
- cd (Change Directory): Moves to a different directory.
  - To Documents: cd Documents moves to the Documents directory inside the current directory.
  - To Root: cd / moves to the root directory.
  - To Home: cd or cd ~ moves to the user's home directory, here /home/user.
  - Up One Level: cd .. moves to the parent directory of the current directory.

### Paths

- Absolute Path: Begins with /, relative to the root directory.
  - Example: /home/user/Documents
- Relative Path: Relative to the current directory.
  - Example: Documents (if the current directory is /home/user).
- Tilde (~): Represents the home directory.
  - Example: ~/Documents is equivalent to /home/user/Documents.
- Dot (.): Represents the current directory.
  - Example: ./Documents refers to the Documents directory in the current directory.
- Double Dot (..): Represents the parent directory.
  - Example: ../../ from /home/user/Documents would refer to /home.

## Files

- Everything is a File:
  - In Linux, everything is treated as a file. This includes not just typical files and directories but also hardware like keyboards and monitors. This unified approach simplifies interactions with different system components.
- Extensionless System:
  - Linux does not rely on file extensions to determine file types. It looks inside the file to understand its nature. This means that changing the extension of a file in Linux does not change how the system treats it, unlike in systems like Windows.
- Case Sensitivity:
  - Linux is case sensitive when it comes to file and directory names. This means FILE1.txt, File1.txt, and file1.TXT are seen as distinct entities. This is a critical aspect to remember, as it affects how you access and manage files.
- Spaces in Names:
  - Linux allows spaces in file and directory names, but they require careful handling. Spaces are used to separate command line arguments, so file names with spaces must be enclosed in quotes (like 'Holiday Photos') or use an escape character (like Holiday\ Photos) to be properly recognized as a single entity.
- Hidden Files and Directories:
  - In Linux, any file or directory whose name begins with a dot (.) is considered hidden. This is a simple yet effective way to hide configuration files and other sensitive data from plain sight. These hidden files are not listed by default when using commands like ls, unless specific options (like -a) are used.
- Path as a File:
  - The concept of a path in Linux is essentially a means to reach a particular file location. Since directories are also files, every path, whether to a file or directory, is a way to access a specific file structure within the Linux system.

## Manual Pages

Manual pages, commonly referred to as "man pages," in Linux, are comprehensive documentation for commands available in the system. They explain each command's purpose, how to run it, and the command line arguments it accepts. The structure of man pages is consistent, making them easier to understand once you're familiar with the format.

To access a man page, use the command man \<command to look up\>. For example, man ls will show the manual page for the ls command. This page typically includes the command name, a brief description, a synopsis outlining how to run the command with various options, and a detailed description of the command and its options.

Additionally, you can search within the manual pages. A keyword search across all man pages is possible with man -k \<search term>. While viewing a man page, you can search for a specific term by pressing /, typing your search term, and hitting 'enter'. Pressing 'n' allows you to cycle through multiple instances of the term.

Man pages also explain command line options, which modify the behavior of commands. These options often come in both long and short forms (e.g., -a or --all for the ls command). Understanding these options is key to being proficient in Linux command line usage.

## File Manipulation

- Making a Directory:
  - Use mkdir [options] \<Directory> to create directories.
  - mkdir makes a directory based on the specified path, which can be relative or absolute.
  - Options include -p (create parent directories as needed) and -v (verbose mode, showing what is being done).
- Removing a Directory:
  - Use rmdir [options] \<Directory> to remove directories.
  - Directories must be empty to use rmdir.
  - Options include -v (verbose) and -p.
- Creating a Blank File:
  - Use touch [options] \<filename> to create a new, empty file.
  - touch can also update file access and modification times.
- Copying a File or Directory:
  - Use cp [options] \<source> \<destination> to copy files or directories.
  - For directories, use -r (recursive) to copy all contents.
  - cp supports both absolute and relative paths for source and destination.
- Moving a File or Directory:
  - Use mv [options] \<source> \<destination> to move or rename files/directories.
  - Moving directories doesn't require additional options.
  - Both source and destination are specified as paths.
- Renaming Files and Directories:
  - Use mv with the source and a new name in the same directory to rename.
  - Can use absolute or relative paths.
- Removing a File (and Non-Empty Directories):
  - Use rm [options] \<file> to remove files.
  - To remove non-empty directories, use rm -r [options] \<directory>.
  - -r stands for recursive, removing all contents within.
  - Option -i (interactive) prompts before each removal.

## Cheat Sheet

[Sheet](https://ryanstutorials.net/linuxtutorial/cheatsheet.php)
