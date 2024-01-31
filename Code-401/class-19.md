# Class 19

## re

Regular expressions are an extremely useful tool to find/match strings. 
```
import re
```

Cheatsheet:
| Metacharacter | Description |
|---------------|-------------|
| .             | A period. Matches any single character except the newline character. |
| ^             | A caret. Matches a pattern at the start of the string. |
| \A            | Uppercase A. Matches only at the start of the string. |
| $             | Dollar sign. Matches the end of the string. |
| \Z            | Uppercase Z. Matches only at the end of the string. |
| [ ]           | Matches the set of characters you specify within it. |
| \             | - If the character following the backslash is a recognized escape character, then the special meaning of the term is taken. - Else the backslash () is treated like any other character and passed through. - It can be used in front of all the metacharacters to remove their special meaning. |
| \w            | Lowercase w. Matches any single letter, digit, or underscore. |
| \W            | Uppercase W. Matches any character not part of \w (lowercase w). |
| \s            | Lowercase s. Matches a single whitespace character like: space, newline, tab, return. |
| \S            | Uppercase S. Matches any character not part of \s (lowercase s). |
| \d            | Lowercase d. Matches decimal digit 0-9. |
| \D            | Uppercase D. Matches any character that is not a decimal digit. |
| \t            | Lowercase t. Matches tab. |
| \n            | Lowercase n. Matches newline. |
| \r            | Lowercase r. Matches return. |
| \b            | Lowercase b. Matches only the beginning or end of the word. |
| +             | Checks if the preceding character appears one or more times. |
| *             | Checks if the preceding character appears zero or more times. |
| ?             | - Checks if the preceding character appears exactly zero or one time. - Specifies a non-greedy version of +, * |
| { }           | Checks for an explicit number of times. |
| ( )           | Creates a group when performing matches. |
| < >           | Creates a named group when performing matches. |

| Function              | Description                                                  |
|-----------------------|--------------------------------------------------------------|
| `re.search(pattern, string)` | Searches the string for a match and returns a match object if found, else returns `None`. |
| `re.match(pattern, string)` | Checks if the pattern matches at the beginning of the string and returns a match object, else returns `None`. |
| `re.fullmatch(pattern, string)` | Checks if the pattern matches the entire string and returns a match object, else returns `None`. |
| `re.findall(pattern, string)` | Finds all occurrences of the pattern in the string and returns them as a list of strings. |
| `re.finditer(pattern, string)` | Finds all occurrences of the pattern in the string and returns them as an iterator of match objects. |
| `re.sub(pattern, replacement, string)` | Replaces occurrences of the pattern with the specified replacement in the string. |
| `re.split(pattern, string)` | Splits the string into a list using the specified pattern as the delimiter. |
| `re.compile(pattern)` | Compiles a regular expression pattern into a regex object for more efficient matching operations. |
| `match.group([group1, ...])` | Returns one or more subgroups of the match. If no argument is provided, returns the entire match. |
| `match.start([group])` | Returns the start position of the match or a specific group in the string. |
| `match.end([group])` | Returns the end position of the match or a specific group in the string. |
| `match.span([group])` | Returns a tuple containing the start and end positions of the match or a specific group in the string. |
| `re.IGNORECASE` | Flag that makes matching case-insensitive. |
| `re.MULTILINE` | Flag that allows the start and end metacharacters (^ and $) to match the start and end of each line. |
| `re.DOTALL` | Flag that allows the dot (.) metacharacter to match any character, including newline. |
| `re.VERBOSE` | Flag that allows the use of whitespace and comments within the pattern for better readability. |

## shutil

The shutil module in Python provides high-level file operations, including copying, archiving, and other file-related tasks.

### Copying Files:
- `copyfile(src, dst)`: Copies the contents of the source file to the destination file.
- `copyfileobj(fsrc, fdst[, length])`: Copies the contents from the open file handles `fsrc` to `fdst`.

### Working with File Metadata:
- `copy()`: Copies a file to a destination. If the destination is a directory, a new file is created in that directory.
- `copy2(src, dst)`: Works like `copy()`, but includes access and modification times in the metadata.

### Copying File Permissions and Metadata:
- `copymode(src, dst)`: Copies the permissions from the source file to the destination file.
- `copystat(src, dst)`: Copies all file metadata (permissions and timestamps) from the source to the destination.

### Working with Directory Trees:
- `copytree(src, dst[, symlinks=False, ignore=None, copy_function=copy2, ...])`: Recursively copies a directory and its contents to a new location.
- `rmtree(path[, ignore_errors=False, onerror=None])`: Removes a directory and its contents.

### Moving Files and Directories:
- `move(src, dst)`: Moves a file or directory from one location to another.

### Finding Files:
- `which(cmd[, mode=os.F_OK | os.X_OK, path=None])`: Finds the path to an executable file in the system's PATH.

### Working with Archives:
- `get_archive_formats()`: Returns supported archive formats for creating archives.
- `make_archive(base_name, format, root_dir=None, base_dir=None, verbose=0, dry_run=0, logger=None)`: Creates a new archive file.
- `unpack_archive(filename[, extract_dir[, format]])`: Extracts the contents of an archive file.

### File System Space:
- `disk_usage(path)`: Returns disk usage statistics for the specified path.

## os

The `os` module in Python provides portable access to operating system-specific features. It wraps platform-specific modules such as posix, nt, and mac, offering some level of portability. The module primarily deals with creating and managing processes and handling file system content.

### File System Operations

- `listdir()`: Lists contents of a directory.
- `walk()`: Recursively traverses a directory.
- `scandir()`: More efficient than `listdir()`, provides additional information.

### File System Permissions

- `stat()`: Provides detailed information about a file.
- `chmod()`: Changes file permissions.
- `access()`: Tests access rights for a file.

### Directories

- `makedirs()`: Creates directories recursively.
- `rmdir()`: Removes leaf directory.
- `removedirs()`: Removes directories along the path.

### Symbolic Links

- `symlink()`: Creates a symbolic link.
- `readlink()`: Reads the original file pointed to by the link.

### Process Management

- `fork()`: Creates a new process.
- `kill()`: Sends signals to processes.
- `wait()`: Waits for any child process to exit.
- `waitpid()`: Waits for a specific child process to exit.

### Environment and Working Directory

- `environ`: Manages environment variables.
- `getcwd()`: Gets the current working directory.
- `chdir()`: Changes the current working directory.

### External Commands

- `system()`: Runs an external command, blocks until completion.

### Error Handling

- `strerror()`: Translates error codes to message strings.

### Spawning New Processes

- `spawnlp()`: Handles fork() and exec() in one statement.

## Things I want to know more about
