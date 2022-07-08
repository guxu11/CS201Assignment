## 1. Overview

.

├── README.md

├── SortingArrays.java

└── SortingSearchingHashmap.java

To get the code:

```bash
git clone git@github.com:guxu11/CS201Assignment.git
```



There are two java programs in my assignment folder, `SortingArrays.java` is the solution to **Part 1: Sorting Arrays,** and 	`SortingSearchingHashmap.java` is the solution to **Part 2: Sorting & Searching HashMap**. 

***Make sure the two java programs are under the same path.***

To run the program, just compile them firstly.

```bash
javac *.java
```

then execute the Part1 program with:

```bash
java SortingArrays
```

and execute Part2 with:

```bash
java SortingSearchingHashmap
```

## 2. Implementation

### 2.1 Part 1: Sorting Arrays

The `SortingArrays` class members:

**properties:**
`StateCapitals`: a 2-d array with a shape of 50 * 2
**methods:**

`getStateCapitals`: To attain the peoperty `StateCapitals`.

`printStateCapitals`:  To display the content of the `StateCapitals` array, 5 1-d arrays per line.

`bubbleSort`: To sort the StateCapitals array in the order of capitals. Use `String::compareTo` method to compare two Strings.

`swap`: The helper of bubblesort

`main`:  To call the methods above to achieve the goal of Task 1:

1. Instantiate a `SortingArrays` object.
2. call the `printStateCapitals` to display the array.
3. call `bubbleSort` to sort the array.
4. design a game which displays a state and prompt the user to type in the corresponding capital. If the capital typed in is wrong, the game will display the correct answer. Considering the number of states in American is too large, this game also allow the user to type in "quit" to end up the game. Finally, the game will display the number of questions that answered by the user in total and the number of correct answers. The game is not sensitive to the case of the input words (Alabama and ALABAMA are the same input to the program).



### 2.2 Part2: Sorting & Searching HashMap

 `SortingSearchingHashmap.java `  contains two classes: `SortingSearchingHashmap` and `BST`.

#### 2.2.1 class BST 

The `BST` class contains a inner class called `Node`  which represents a node in the binary search tree. Each node has 4 properties:

```java
String key;   // state
String value; // capital
Node leftChild;
Node rightChild;
```

The `BST` class contains 2 properties:

```java
Node root;  // root node
int size;   // size of the tree
```

and contains 4 methods:

`size`: To get the property size.

`insertNode`:  A recursive method and a helper to insert a node. Use `campareTo` method to compare two Strings.

`insert`:  Call the insertNode method to insert a key-value pair.

`findNode`:  To figure out if there exist a node with a certain key in the binary search tree.



#### 2.2.2 class SortingSearchingHashmap

The `SortingSearchingHashmap`  members:

**properties**:

`stateCapitalMap`: A hashmap whose key represents a state and value a correspond capital. The content of the hashmap stem from the 2-d array `StateCapitals` in class `SortingArrays`

**methods:**

`getStateCapitalMap`: To get stateCapitalMap.

`printStateCapitalMap`: To display the content of stateCapitalMap.

`sortWithTreeMap`: To sort the key-value pairs (Entries) by converting stateCapitalMap to a treemap.

`storeStateCapitalInABST`: To instantiate a `BST` object and call the `insert` method to store the key-value pairs.

`main`:  To call the methods above to achieve the goal of Task 2:

1. Instantiate a `SortingSearchingHashmap` object.

2. call the `printStateCapitalMap` method to display the key-value pairs.
3. call the `sortWithTreeMap` to sort the key-value pairs.
4. call the `storeStateCapitalInABST` to store the key-value pairs in a BST.
5. design a game where after a user typing a state, its capital will be shown. if the user want to end up this game, just type in "quit". The game is not sensitive to the case of the input words (Alabama and ALABAMA are the same input to the program).

 



