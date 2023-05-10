# dup_file_rust_mono
Duplicate file finder/remover - a monolithic rust application

# Install

### Compiling the binary
Clone the repository and build manually:

```
$ mkdir -p ~/github.com/dup_file_rust_mono
$ cd ~/github.com/dup_file_rust_mono
$ git clone https://github.com/FileSystemTools/dup_file_rust_mono.git
$ cd dup_file_rust_mono
$ cargo build
$ target/dup_file_rust_mono
```

## Functional Requirements
1. Take a list of directories to scan for files
2. Take a list of filters to select/ignore files within the directories
3. Output the path/name of duplicate files to stdout or named output file
4. Delete the duplicate files (leaving only one instance) if the user selecte autodelete action
5. Store the list of files visited in such a way to avoid needing reading unchanged files during next iteration

## Non-Functional Requirements
1. Do not hog too much CPU (not more than 30%?)
2. Single threaded is OK
3. Use multi-threading but do not go beyond 2 * CPU core
4. HOw much memory should the app use (% of total memory or absolute ceiling)