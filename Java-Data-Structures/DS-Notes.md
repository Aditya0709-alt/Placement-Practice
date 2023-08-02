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


### List

- An ordered collection of elements
- Allows duplicates
- Variable sized
- Several implementations -> ArrayList, Stack, Vector

  ```java
  List<String> list = new ArrayList<>();

        list.add("a");
        list.add("b");
        list.add("okurr");


        System.out.println(list);
        System.out.println(list.size());

        list.forEach(System.out::println);
  ```

- The '<>' operator or diamond operator is used for type inference allowing the compiler to infer the type
- List.of() method returns immutable collection of elements


### Stack

- LIFO pattern
- Extends 'Vector' class
- Operations -> push, pop, peek

```java
import java.util.Stack;

public class Stack_DS {
    public static void main(String[] args) {
        Stack<Integer> stack = new Stack<>();

        stack.push(1);
        stack.push(2);
        System.out.println(stack);
        System.out.println(stack.size());
        System.out.println(stack.peek());
        System.out.println(stack.empty());
    }
}
```

### Queue

- FIFO pattern
