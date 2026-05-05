# 🔢 Sorting & Searching Algorithms — Java Demo

A Java playground demonstrating classic **sorting** and **searching** algorithms implemented from scratch. This project was created for learning and demonstration purposes, covering Bubble Sort, Quick Sort, and a side-by-side comparison of Linear Search vs. Binary Search with step counting.

---

## 📁 Project Structure

```
Demo/
└── src/
    ├── BubbleSort.java   # Bubble sort with step-by-step output
    ├── QuickSort.java    # Recursive quick sort with partition
    ├── Merge.java        # Merge sort (stub / work in progress)
    └── Search.java       # Linear search vs. binary search with step counter
```

---

## 🧮 Algorithms Covered

### 🫧 Bubble Sort — `BubbleSort.java`

Sorts the array `{6, 5, 2, 8, 9, 4}` in ascending order using the classic adjacent-swap approach. Prints the array state after **every pass** so you can watch the elements bubble into place.

**How it works:** Repeatedly compares adjacent pairs and swaps them if they are out of order. Each outer pass guarantees the next largest element is in its final position.

**Time Complexity:** O(n²) average and worst case

**Sample Output:**
```
Before sorting
6 5 2 8 9 4
5 2 6 8 4 9
2 5 6 4 8 9
2 5 4 6 8 9
2 4 5 6 8 9
2 4 5 6 8 9
After sorting
2 4 5 6 8 9
```

---

### ⚡ Quick Sort — `QuickSort.java`

Sorts the array `{5, 6, 2, 3, 1, 8, 4}` using the **Lomuto partition scheme** with the last element as the pivot. Implemented recursively with a separate `partition()` method.

**How it works:** Picks a pivot, partitions the array so all elements less than the pivot come before it and all greater elements come after, then recursively sorts the two sub-arrays.

**Time Complexity:** O(n log n) average, O(n²) worst case

**Sample Output:**
```
1 2 3 4 5 6 8
```

---

### 🔍 Linear Search vs. Binary Search — `Search.java`

Searches for the value `900` in an array of 1000 integers, running **both algorithms** on the same input and reporting the number of steps each one takes — making the efficiency difference immediately visible.

| Algorithm | Approach | Time Complexity |
|---|---|---|
| Linear Search | Scans from index 0 to end | O(n) |
| Binary Search | Halves the search space each step | O(log n) |

> Binary Search requires a sorted array. The demo uses a zero-filled array (`new int[1000]`) where `900` is not present, so both algorithms run to completion — showing their worst-case step counts.

**Sample Output:**
```
Steps taken by binarySearch: 10
Steps taken by linearSearch: 1000
Element not found
```

---

### 🔀 Merge Sort — `Merge.java`

Stub class — implementation is a work in progress.

---

## 🛠️ Tech Stack

- **Language:** Java
- **IDE:** IntelliJ IDEA
- **No external dependencies** — pure Java standard library

---

## 🚀 Getting Started

### Prerequisites

- JDK 8 or higher

### Run via Command Line

```bash
# Clone the repository
git clone https://github.com/Trovz/Demo.git
cd Demo/src

# Compile all files
javac *.java

# Run any of the demos
java BubbleSort
java QuickSort
java Search
```

### Run in IntelliJ IDEA

1. Open the `Demo` folder in IntelliJ IDEA.
2. Navigate to `src/` and open the file you want to run.
3. Click the **▶ Run** button next to the `main` method, or press `Shift + F10`.

---

## 🔑 Key Concepts Demonstrated

| Concept | Where |
|---|---|
| Nested loops and swap logic | `BubbleSort.java` |
| Recursion and divide-and-conquer | `QuickSort.java` |
| Lomuto partition scheme | `QuickSort.java` |
| Sequential vs. logarithmic search | `Search.java` |
| Step-count instrumentation | `Search.java` |
| Algorithm efficiency comparison | `Search.java` |
