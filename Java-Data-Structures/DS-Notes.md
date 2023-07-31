## Java Data Structures

### Array
- Fixed in size
- Fast for data retrievals
- Compact memory usage if size is known
- Delete operation very hard
- Can be passed as varargs

```java
// Method with varargs
void printNumbers(int... numbers) {
    for (int num : numbers) {
        System.out.println(num);
    }
}

// Calling the method with an array
int[] myArray = {1, 2, 3};
printNumbers(myArray);

// Calling the method with individual elements
printNumbers(4, 5, 6);
```

Array implementation

```java
public static void printNumbers (int ...numbers) {
        for(int num: numbers){
            System.out.print(num + " ");
        }
    }
    public static void main(String[] args) {
        printNumbers(1, 2, 3);

        String [] colors = new String [3];
        colors[0] = "purple";
        colors[1] = "blue";
        colors[2] = "green";

        for(String color: colors) {
            System.out.println(color);
        }
        // Method reference operator (behaves like lambda expressions)
        Arrays.stream(colors).forEach(System.out::println);
```

2-D Array implementation

```java

int m = 5;
        int n = 5;
        char[][] arr = new char[m][n];
        for (int i = 0; i < m; i++) {
            for (int j = 0; j < n; j++) {
                arr[i][j] = '-';
            }
        }

        int[][] board = new int[][]{
                new int[]{1, 2, 3},
                new int[]{4, 5, 6}
        };

        System.out.println(Arrays.deepToString(board));

        arr[0][0] = 'O';
        arr[1][0] = 'O';
        arr[2][0] = 'O';

        System.out.println(Arrays.deepToString(arr));
```

- java.utils.Arrays interface -> contains utility methods for arrays
