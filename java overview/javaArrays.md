# Working with Arrays in Java

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


###Example program:
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

