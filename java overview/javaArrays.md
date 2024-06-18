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
