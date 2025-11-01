# Columbia River Binary Tree Project

---

[cite_start]This project models the **Columbia River** and its vast watershed using a **binary tree structure** [cite: 6] [cite_start]implemented in **C++**[cite: 6]. [cite_start]The program allows for traversal of river features, addition of new tributaries and dams, and the output of key system information[cite: 7].

| Project Team |
| :--- |
| [cite_start]Carson Frost, Joe Mock, Charlie Serafin, Jessica Sun [cite: 3] |

---

## Running the Program

### Compile and Run

To compile and run the main program:

1.  [cite_start]Compile: ``$g++$ main.cpp RiverTree.cpp-o program`` [cite: 9]
2.  [cite_start]Run: ``./program.exe`` [cite: 9]

### Running Unit Tests

To compile and run the unit tests:

1.  [cite_start]Compile: ``g++ unit\_test.cpp RiverTree.cpp-o test`` [cite: 11]
2.  [cite_start]Run: ``./test.exe`` [cite: 12]

---

## System Design & Structure

[cite_start]The river system is modeled as a binary tree, where each **RiverNode** object stores either a **tributary** or a **dam**, but never both[cite: 30].

* [cite_start]**Root Node:** Represents the Columbia River's mouth and serves as the tree's entry point[cite: 31].
* [cite_start]**Tributaries:** Always branch to the **right child node** of their parent[cite: 24, 37].
* [cite_start]**River Continuation:** The river continues along the path to the **left child node** (if a right node exists)[cite: 25, 37]. [cite_start]This design makes the tree more like an actual river system while maintaining the binary tree structure[cite: 38].


---

## Program Features (Menu)

[cite_start]Users select their choice from the menu by typing a number from 1-5[cite: 13]:

* [cite_start]**View Full Tree (1):** Prints the full tree [cite: 15, 41][cite_start], with the root furthest to the right, and leaf nodes toward the left[cite: 42]. [cite_start]This uses a basic **in-order traversal** structure for printing[cite: 44].
* [cite_start]**Explore Tree (2):** The user is presented one node at a time with all relevant information and can move from node to node along connections[cite: 16, 91].
* [cite_start]**Print All Dams (3):** Lists every node whose name contains "Dam," along with the river each dam belongs to[cite: 17, 95].
* [cite_start]**Add Node (Interactive) (4):** Allows the user to add a new node to the system by specifying the parent river, choosing whether to add a dam or a tributary, and entering the required details[cite: 18, 96, 97, 98, 99, 100].
* [cite_start]**Quit (5):** Exits the program[cite: 19, 103, 104].

---

### **Attributes Stored in Nodes**

The project stores specific attributes for tributaries and dams:

| Node Type | Attributes Stored | Note |
| :--- | :--- | :--- |
| **Tributary** | [cite_start]Length, Basin Size, Discharge [cite: 28] | [cite_start]Fake, roughly approximated values are used primarily to show the opportunity for information storage and display[cite: 29]. |
| **Dam** | [cite_start]Relevant attributes (not explicitly detailed, but different from tributary info) [cite: 27, 34] | [cite_start]The design includes separate constructors for Dams and Tributaries because their required information is different[cite: 33, 34]. |

---
