# Algorithm Battle – Which Data Structure Wins?

## Student details
- **Name:** Murugesan M
- **Register Number:** RA2511042050009

## Project overview
A C-based Student Record Management System comparing:
- **Binary Search Tree (BST)** for ordered record storage.
- **AVL Tree** for self-balancing search.
- **Hash Table with Linear Probing** for key-based lookup.

Each record contains a Student ID, name, department and marks.

## Dataset
The program uses 30 records in a mixed insertion order. IDs range from 3201 to 3297.

| Student ID | Name | Department | Marks |
|---:|---|---|---:|
| 3201 | Aadhav | CSE | 86 |\n| 3217 | Bhuvan | ECE | 78 |\n| 3234 | Chandru | IT | 92 |\n| 3250 | Dharun | EEE | 81 |\n| 3268 | Ezhilan | AIML | 95 |\n| 3285 | Farooq | CSE | 73 |\n| 3209 | Girish | ECE | 88 |\n| 3226 | Harith | IT | 90 |\n| 3243 | Iniyan | EEE | 84 |\n| 3261 | Jeevan | AIML | 97 |\n| 3278 | Kavin | CSE | 76 |\n| 3292 | Logesh | ECE | 89 |\n| 3212 | Mithun | IT | 93 |\n| 3229 | Naren | EEE | 80 |\n| 3247 | Pranav | AIML | 85 |\n| 3265 | Rithik | CSE | 91 |\n| 3281 | Sathish | ECE | 74 |\n| 3297 | Tharun | IT | 87 |\n| 3205 | Udhay | EEE | 96 |\n| 3221 | Vimal | AIML | 82 |\n| 3238 | Yogesh | CSE | 94 |\n| 3256 | Akhil | ECE | 79 |\n| 3273 | Balaji | IT | 90 |\n| 3289 | Charan | EEE | 83 |\n| 3210 | Dinesh | AIML | 88 |\n| 3224 | Gokul | CSE | 75 |\n| 3240 | Hari | ECE | 98 |\n| 3259 | Karthi | IT | 86 |\n| 3276 | Mani | EEE | 92 |\n| 3294 | Nithish | AIML | 81 |\n
## Operations
1. Search using BST
2. Search using AVL Tree
3. Search using Hashing
4. Display BST traversals
5. Display AVL traversals
6. Display Hash Table
7. Insert a new student
8. Run performance experiment
9. Display all student records
0. Exit

## Configuration
| Parameter | Value |
|---|---|
| Initial records | 30 |
| Maximum capacity | 100 |
| Hash table size | 47 |
| Hash function | `h(id) = id % 47` |
| Collision handling | Linear probing |
| Successful search key | 3265 |
| Unsuccessful search key | 3399 |

## Measured performance
These values were obtained by compiling and running the supplied `student.c` with the dataset above.

| Measurement | BST | AVL Tree | Hash Table |
|---|---:|---:|---:|
| Height (nodes) | 9 | 6 | Not applicable |
| Successful search (3265) | 7 comparisons | 4 comparisons | 1 probe |
| Unsuccessful search (3399) | 8 comparisons | 5 comparisons | 5 probes |
| Insertion collisions | Not applicable | Not applicable | 11 |

The results depend on the insertion order and hash function. The mixed order avoids a fully skewed BST, while the AVL tree maintains balance. The modulo-47 hash function has 11 collisions for this dataset.

## Compile and run
```bash
gcc -std=c99 -Wall -Wextra student.c -o student
./student
```
On Windows with GCC/MinGW:
```bash
gcc -std=c99 -Wall -Wextra student.c -o student.exe
student.exe
```

## Repository structure
```text
Algorithm_Battle_Submission/
├── student.c
├── README.md
├── report.docx
└── Screenshots/
    ├── initial_dataset.png
    ├── bst_successful_search_3265.png
    ├── avl_successful_search_3265.png
    ├── hash_successful_search_3265.png
    ├── bst_unsuccessful_search_3399.png
    ├── avl_unsuccessful_search_3399.png
    ├── hash_unsuccessful_search_3399.png
    ├── bst_traversals.png
    ├── avl_traversals.png
    ├── hash_table.png
    ├── performance_comparison.png
    └── insert_student_3301.png
```

## GitHub reference
https://github.com/murugesh0715/algorithm_battle

The GitHub URL is a reference link. The files in this ZIP are a separate locally revised copy.
