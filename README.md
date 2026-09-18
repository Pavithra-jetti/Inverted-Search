# Inverted Search in C

## Overview

This project is an **Inverted Search (Indexing) application developed in C**. It reads multiple text files, builds an inverted index (a hash table mapping each word to the files and counts in which it occurs), and lets users search for a word to see which files it appears in and how often.

The project demonstrates the practical use of **hash tables, linked lists, nested data structures, dynamic memory allocation, and file handling** in C, and models the indexing and search functionality used in search engines.

## Features

* Indexes words from multiple input text files
* Builds a hash-table-based inverted index using 26 buckets (A–Z)
* Searches for a word and displays every file in which it appears with occurrence count
* Displays the complete inverted index database
* Saves the database to disk for later use
* Retrieves a previously saved database
* Updates the existing database with new files
* Menu-driven interface with input file validation
* Build automation using `makefile`

## Technologies Used

* **Programming Language:** C
* **Compiler:** GCC
* **Platform:** Linux / Windows
* **Concepts:** Hash Tables, Linked Lists, Nested Structures, Dynamic Memory Allocation, File Handling
* **Libraries:** `stdio.h`, `stdlib.h`, `string.h`, `ctype.h`
* **Build Tool:** `make`

## Project Structure

```text
Inverted-Search-in-C/
│
├── main.c
├── inv.h
├── create.c
├── display.c
├── search.c
├── save_update.c
├── retrieve.c
├── database.txt
├── f1.txt
├── f2.txt
├── f3.txt
├── makefile
├── README.md
└── .gitignore
```

### File Description

| File                | Description                                                                                   |
| ------------------- | --------------------------------------------------------------------------------------------- |
| `main.c`            | Program entry point; validates input files and drives the menu                                |
| `inv.h`             | Contains `main_node`, `sub_node`, and `Slist` structure definitions and function declarations |
| `create.c`          | Builds the inverted index (hash table) from the input files                                   |
| `display.c`         | Displays the complete inverted index database                                                 |
| `search.c`          | Searches the database for a given word                                                        |
| `save_update.c`     | Saves the current database to disk and updates it with new files                              |
| `retrieve.c`        | Loads a previously saved database into memory                                                 |
| `database.txt`      | Stores the persisted inverted index data                                                      |
| `f1.txt` – `f3.txt` | Sample input text files used to test indexing and search                                      |
| `makefile`          | Build rules to compile all modules and link the final executable                              |
| `README.md`         | Project documentation                                                                         |
| `.gitignore`        | Specifies generated files that should not be uploaded to GitHub                               |

## How to Run

### 1. Clone the Repository

Open **Command Prompt / Terminal** and run:

```bash
git clone <your-github-repository-link>
```

### 2. Open the Project Directory

```bash
cd Inverted-Search-in-C
```

### 3. Compile the Program

Using the makefile:

```bash
make
```

Or manually:

```bash
gcc main.c create.c display.c search.c save_update.c retrieve.c -o Inv.out
```

### 4. Run the Program

```bash
./Inv.out f1.txt f2.txt f3.txt
```

## Run

After launching with one or more input files, a menu is displayed:

```text
1. Create Database
2. Search Word
3. Display Database
4. Save Database
5. Update Database
6. Retrieve Database
7. Exit
```

The user can select an option to build the index, search for a word across the loaded files, display or save the database, update it with new files, or retrieve a previously saved database.

To clean up build artifacts:

```bash
make clean
```

## Learning Outcomes

* Gained practical understanding of how inverted indexes support search functionality
* Learned to design and implement a hash table in C
* Practiced combining linked lists with hash-table buckets
* Improved understanding of dynamic memory allocation and pointer management
* Learned persistent storage techniques for saving and retrieving in-memory data
* Practiced build automation using `make` and a `makefile`
* Improved debugging and problem-solving skills

## Author

**Pavithra Jetti**
