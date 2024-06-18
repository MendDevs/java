# Working with Arrays in Java

## A. Arrays
### 1. Declaring and Initializing Arrays

#### 1D Array:
```java
// Declaration
int[] numbers;

// Initialization
numbers = new int[5]; // Array of 5 integers

// Combined Declaration and Initialization
int[] numbers = new int[5];
```
#### 2D Array:

```java
// Declaration
int[][] matrix;

// Initialization
matrix = new int[3][4]; // 3 rows, 4 columns

// Combined Declaration and Initialization
int[][] matrix = new int[3][4];
```

### 2. Assigning Values to Arrays

#### 1D Array:
```java
int[] numbers = new int[5];
numbers[0] = 10;
numbers[1] = 20;
numbers[2] = 30;
numbers[3] = 40;
numbers[4] = 50;

// Alternative Initilizatoin

int[] numbers = {10,20,30,40,50};

```

#### 2D Array:
```java
int[][] matrix = new int[3][4];
matrix[0][0] = 1;
matrix[0][1] = 2;
//.. and so on

//Alternative Initialization
int[]p] matrix = {
    {1,2,3,4},
    {5,6,7,8},
    {9,10,11,12}
};
```

### 3. Accessing Array Elements
#### 1D Array:
```java
    int firstNumber = nubers[0];
    System.out.println("First number: "+ firstNumber);
```

#### 2D Array
```java
int element = matrix[1][2];
System.out.println("Element at row 1, column 2: " + element);
```

### 4. Looping Through Arrays
#### 1D Array
```java
int[] numbers = {10, 20, 30, 40, 50};

//Using for loop
for (int i=0; i<numbers.length; i++){
    System.out.println(numbers[i]);
}

// Using enhanced for loop
for (int i : numbers){
    System.out.println(number);
}
```

#### 2D Array
```java
int[][] matrix = {
    {1, 2, 3, 4},
    {5, 6, 7, 8},
    {9, 10, 11, 12}
};

// Using nested for loops
for (int i = 0; i< matrix.length; i++){
    for(int j = 0; j< matrix[i].length; j++){
        System.out.print(matrix[i][j] + " ");
    }
    System.out.println();
}

//Using enhanced for loop
for (int[] row : matrix){
for (int element : row) {
    System.out.print(element + " ");
 }
    System.out.println();
}
```

### 5. Common Array Operations

#### Finding the length:
```java
    int length = numbers.length; //for 1D array
    int rows = matrix.length; // number of rows for 2D array
    int columns = matrix[0].length; // number of columns for 2D array
```

#### Copying an Array
```java
    int[] copy = Arrays.copyOf(numbers, numbers.length);
```

#### Sorting an Array
```java
    Arrays.sort(numbers);
```

#### Seraching an Array
```java
int index = Arrays.binarySearch(numbers, 30); // Array must be sorted before binary search
```


### Example program:
```java
import java.util.Arrays;

public class ArrayExample {
    public static void main(String[] args) {
        // 1D Array
        int[] numbers = {10, 20, 30, 40, 50};
        System.out.println("1D Array:");
        for (int number : numbers) {
            System.out.println(number);
        }

        // 2D Array
        int[][] matrix = {
            {1, 2, 3, 4},
            {5, 6, 7, 8},
            {9, 10, 11, 12}
        };
        System.out.println("\n2D Array:");
        for (int[] row : matrix) {
            for (int element : row) {
                System.out.print(element + " ");
            }
            System.out.println();
        }

        // Copying an Array
        int[] copy = Arrays.copyOf(numbers, numbers.length);
        System.out.println("\nCopied Array: " + Arrays.toString(copy));

        // Sorting an Array
        Arrays.sort(numbers);
        System.out.println("\nSorted Array: " + Arrays.toString(numbers));

        // Searching an Array
        int index = Arrays.binarySearch(numbers, 30);
        System.out.println("\nIndex of 30: " + index);
    }
}
```


## B. Array Lists

### 1D Array Lists

#### 1. Importing Necessary Classes
To work with lists, you need to import the required classes from the `java.util` package:
```java
import java.util.ArrayList;
import java.util.LinkedList;
import java.util.List;
import java.util.Iterator;
```

#### 2. Creating a List
You can create a `List<Integer>` using various implementations. The most common are `ArrayList` and `LinkedList`.

```java
List<Integer> arrayList = new ArrayList<>();
List<Integer> linkedList = new LinkedList<>();
```

#### 3. Adding Elements
You can add elements to the list using the `add` method.

```java
arrayList.add(10);
arrayList.add(20);
arrayList.add(30);
```

#### 4. Accessing Elements
You can access elements using the `get` method and the index of the element.

```java
int firstElement = arrayList.get(0); // Returns 10
int secondElement = arrayList.get(1); // Returns 20
```

#### 5. Iterating Over Elements
You can iterate over the elements of the list using different methods such as a `for` loop, enhanced `for` loop, `Iterator`, or `forEach`.

##### Using a For Loop
```java
for (int i = 0; i < arrayList.size(); i++) {
    System.out.println(arrayList.get(i));
}
```

##### Using an Enhanced For Loop
```java
for (Integer element : arrayList) {
    System.out.println(element);
}
```

##### Using an Iterator
```java
Iterator<Integer> iterator = arrayList.iterator();
while (iterator.hasNext()) {
    System.out.println(iterator.next());
}
```

##### Using forEach with Lambda Expression
```java
arrayList.forEach(element -> {
    System.out.println(element);
});
```

#### 6. Modifying Elements
You can modify elements using the `set` method.

```java
arrayList.set(1, 25); // Changes the element at index 1 to 25
```

#### 7. Removing Elements
You can remove elements by index or by value.

##### Removing by Index
```java
arrayList.remove(1); // Removes the element at index 1
```

##### Removing by Value
```java
arrayList.remove(Integer.valueOf(30)); // Removes the first occurrence of the value 30
```

#### 8. Checking If an Element Exists
You can check if the list contains a particular element using the `contains` method.

```java
boolean contains10 = arrayList.contains(10); // Returns true if 10 is in the list
```

#### 9. Getting the Size of the List
You can get the number of elements in the list using the `size` method.

```java
int size = arrayList.size(); // Returns the number of elements in the list
```

#### 10. Clearing the List
You can remove all elements from the list using the `clear` method.

```java
arrayList.clear();
```

#### Example Code
Here is a complete example that demonstrates these operations:

```java
import java.util.ArrayList;
import java.util.Iterator;
import java.util.List;

public class Main {
    public static void main(String[] args) {
        // Create a List using ArrayList
        List<Integer> arrayList = new ArrayList<>();

        // Add elements
        arrayList.add(10);
        arrayList.add(20);
        arrayList.add(30);

        // Access elements
        System.out.println("First element: " + arrayList.get(0));
        System.out.println("Second element: " + arrayList.get(1));

        // Iterate over elements using different methods
        System.out.println("Using for loop:");
        for (int i = 0; i < arrayList.size(); i++) {
            System.out.println(arrayList.get(i));
        }

        System.out.println("Using enhanced for loop:");
        for (Integer element : arrayList) {
            System.out.println(element);
        }

        System.out.println("Using Iterator:");
        Iterator<Integer> iterator = arrayList.iterator();
        while (iterator.hasNext()) {
            System.out.println(iterator.next());
        }

        System.out.println("Using forEach with lambda:");
        arrayList.forEach(element -> {
            System.out.println(element);
        });

        // Modify an element
        arrayList.set(1, 25);
        System.out.println("Modified list: " + arrayList);

        // Remove elements
        arrayList.remove(1); // Removes the element at index 1
        arrayList.remove(Integer.valueOf(30)); // Removes the first occurrence of the value 30
        System.out.println("List after removals: " + arrayList);

        // Check if the list contains an element
        boolean contains10 = arrayList.contains(10);
        System.out.println("List contains 10: " + contains10);

        // Get the size of the list
        int size = arrayList.size();
        System.out.println("Size of the list: " + size);

        // Clear the list
        arrayList.clear();
        System.out.println("List after clearing: " + arrayList);
    }
}
```

### 2D Array Lists

#### 1. Importing Necessary Classes

```java
import java.util.ArrayList;
import java.util.List;
```

#### 2. Creating a 2D ArrayList
You can create a 2D `ArrayList` by first creating an `ArrayList` of `ArrayList` objects.
```java
List<List<Integer>> arrayList2D = new ArrayList<>();
```

#### 3. Adding Elements
You can add rows and then add elements to these rows.

##### Adding Rows
```java
arrayList2D.add(new ArrayList<>());
arrayList2D.add(new ArrayList<>());
```

##### Adding Elements to Rows
```java
arrayList2D.get(0).add(1); // Add 1 to the first row
arrayList2D.get(0).add(2); // Add 2 to the first row
arrayList2D.get(1).add(3); // Add 3 to the second row
arrayList2D.get(1).add(4); // Add 4 to the second row
```

#### 4. Accessing Elements
You can access elements using the `get` method.
```java
int firstElement = arrayList2D.get(0).get(0); // Returns 1
int secondElement = arrayList2D.get(1).get(1); // Returns 4
```

#### 5. Iterating Over Elements
You can iterate over the elements of the 2D list using nested loops.

##### Using Nested For Loops
```java
for (int i = 0; i < arrayList2D.size(); i++) {
    for (int j = 0; j < arrayList2D.get(i).size(); j++) {
        System.out.println(arrayList2D.get(i).get(j));
    }
}
```

##### Using Enhanced For Loops
```java
for (List<Integer> row : arrayList2D) {
    for (Integer element : row) {
        System.out.println(element);
    }
}
```

#### 6. Modifying Elements
You can modify elements using the `set` method.

```java
arrayList2D.get(0).set(0, 10); // Changes the element at (0,0) to 10
```

#### 7. Removing Elements
You can remove elements by index or by value.

##### Removing by Index
```java
arrayList2D.get(0).remove(0); // Removes the element at (0,0)
```

##### Removing by Value
```java
arrayList2D.get(1).remove(Integer.valueOf(4)); // Removes the first occurrence of the value 4 in the second row
```

#### 8. Checking If an Element Exists
You can check if a row contains a particular element using the `contains` method.

```java
boolean contains1 = arrayList2D.get(0).contains(1); // Returns true if 1 is in the first row
```

#### Example Code
Here is a complete example that demonstrates these operations:

```java
import java.util.ArrayList;
import java.util.List;

public class Main {
    public static void main(String[] args) {
        // Create a 2D ArrayList
        List<List<Integer>> arrayList2D = new ArrayList<>();

        // Add rows to the 2D ArrayList
        arrayList2D.add(new ArrayList<>());
        arrayList2D.add(new ArrayList<>());

        // Add elements to the rows
        arrayList2D.get(0).add(1);
        arrayList2D.get(0).add(2);
        arrayList2D.get(1).add(3);
        arrayList2D.get(1).add(4);

        // Access elements
        System.out.println("First element: " + arrayList2D.get(0).get(0)); // 1
        System.out.println("Second element: " + arrayList2D.get(1).get(1)); // 4

        // Iterate over elements using nested for loops
        System.out.println("Using nested for loops:");
        for (int i = 0; i < arrayList2D.size(); i++) {
            for (int j = 0; j < arrayList2D.get(i).size(); j++) {
                System.out.println(arrayList2D.get(i).get(j));
            }
        }

        // Iterate over elements using enhanced for loops
        System.out.println("Using enhanced for loops:");
        for (List<Integer> row : arrayList2D) {
            for (Integer element : row) {
                System.out.println(element);
            }
        }

        // Modify an element
        arrayList2D.get(0).set(0, 10);
        System.out.println("Modified list: " + arrayList2D);

        // Remove elements
        arrayList2D.get(0).remove(0); // Removes the element at (0,0)
        arrayList2D.get(1).remove(Integer.valueOf(4)); // Removes the first occurrence of the value 4 in the second row
        System.out.println("List after removals: " + arrayList2D);

        // Check if the first row contains an element
        boolean contains1 = arrayList2D.get(0).contains(1);
        System.out.println("First row contains 1: " + contains1);

        // Get the size of the 2D list
        int size = arrayList2D.size();
        System.out.println("Size of the 2D list: " + size);

        // Clear the 2D list
        arrayList2D.clear();
        System.out.println("List after clearing: " + arrayList2D);
    }
}
```
## C. Converting from Array Lists to Arrays:


#### 1. Converting a One-Dimensional `ArrayList` to an Array


##### Example Code
```java
import java.util.ArrayList;

public class Main {
    public static void main(String[] args) {
        // Create an ArrayList
        ArrayList<Integer> arrayList = new ArrayList<>();
        arrayList.add(1);
        arrayList.add(2);
        arrayList.add(3);

        // Convert the ArrayList to an array
        Integer[] array = new Integer[arrayList.size()];
        array = arrayList.toArray(array);

        // Print the array
        for (int i : array) {
            System.out.println(i);
        }
    }
}
```

#### 2. Converting a Two-Dimensional `ArrayList` to an Array


##### Example Code
```java
import java.util.ArrayList;
import java.util.List;

public class Main {
    public static void main(String[] args) {
        // Create a 2D ArrayList
        List<List<Integer>> arrayList2D = new ArrayList<>();

        // Add rows to the 2D ArrayList
        arrayList2D.add(new ArrayList<>());
        arrayList2D.add(new ArrayList<>());

        // Add elements to the rows
        arrayList2D.get(0).add(1);
        arrayList2D.get(0).add(2);
        arrayList2D.get(1).add(3);
        arrayList2D.get(1).add(4);

        // Convert the 2D ArrayList to a 2D array
        int[][] array2D = new int[arrayList2D.size()][];
        for (int i = 0; i < arrayList2D.size(); i++) {
            List<Integer> row = arrayList2D.get(i);
            array2D[i] = new int[row.size()];
            for (int j = 0; j < row.size(); j++) {
                array2D[i][j] = row.get(j);
            }
        }

        // Print the 2D array
        for (int[] row : array2D) {
            for (int element : row) {
                System.out.print(element + " ");
            }
            System.out.println();
        }
    }
}
```


