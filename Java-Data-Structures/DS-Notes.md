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
