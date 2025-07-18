---
description: Read and write data to files using Python to add persistence to your programs.
---

# 133 File handling

This module explores how data can be stored permanently by reading from and writing to files. You'll learn to use Python’s file handling functions and understand the importance of persistence in real-world applications.

### Targets

In this topic, students learn to:

* Understand what file persistence means and why it's important
* Read data from a file using Python
* Write data to a file using Python
* Apply file reading/writing to basic text-based data storage tasks
* Use context managers (`with` statement) to handle files safely and efficiently

#### Glossary

| Term                | Definition                                                                                              |
| ------------------- | ------------------------------------------------------------------------------------------------------- |
| **Persistence**     | The ability of a program to save data across multiple runs using external storage like a file           |
| **Text file**       | A file that stores data in human-readable characters, typically ending in `.txt`                        |
| **File handle**     | A variable that references an open file so that it can be read or written to                            |
| **Context manager** | A construct that ensures resources like files are properly opened and closed using the `with` statement |
| **Mode**            | A string passed to `open()` that tells Python whether to read ('r'), write ('w'), append ('a'), etc.    |

Data held in memory is lost when a program ends, but we can store information persistently by saving it to a file. This is useful for everything from saving scores in a game to logging transactions in an app. Python provides built-in methods to interact with files using simple syntax.

We'll focus on text files in this topic. While binary files are also important, they are covered later. Python allows us to open a file, read its contents, write new information, or append to existing data. We'll also introduce the use of the `with` statement, which ensures that files are closed adequately after use, helping prevent data corruption or file locks.

### Reading from a file

You can open and read from a file using the `open()` function and read methods like `.read()`, `.readline()`, or `.readlines()`.

```python
with open("log.txt", "r") as file:
    content = file.read()
    print(content)
```

This reads the entire contents of `"log.txt"` into memory and prints it.

### Writing to a file

To save information, use write mode (`"w"`), which overwrites the file, or append mode (`"a"`), which adds to the end.

```python
with open("log.txt", "w") as file:
    file.write("Log entry 1\n")
    file.write("Log entry 2\n")
```

### Reading line by line

You can loop over each line in a file using:

```python
with open("log.txt", "r") as file:
    for line in file:
        print(line.strip())
```

This is useful when processing structured data, like logs or user input stored in a file.

### Writing lists to a file

Use `.writelines()` to write multiple lines at once:

```python
lines = ["First line\n", "Second line\n"]
with open("log.txt", "w") as file:
    file.writelines(lines)
```

Be careful: `.writelines()` doesn’t add newline characters automatically.

### Best practices

* Always use the `with` statement to open files
* Include newline characters () when writing lines
* Use `"r"` for reading, `"w"` for overwriting, and `"a"` for appending
* Check if a file exists before reading if you're unsure it was created

### Key concepts

* Python uses `open()` to work with files, supporting various modes (`"r"`, `"w"`, `"a"`)
* The `with` statement ensures files are closed properly
* Files allow for persistence of data across sessions
* Reading and writing can be done line-by-line or as a block
* Use `.strip()` to remove trailing newlines or whitespace when reading lines
