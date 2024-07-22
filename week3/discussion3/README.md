# Difference-Arrays-ArrayLists

## Description
This project demonstrates the differences between arrays and ArrayLists in Java. 

## Arrays
Arrays are a fundamental data structure in Java used to store a fixed-size sequential collection of elements of the same type. Once created, the size of an array cannot be changed.

## ArrayLists
ArrayList is part of the Java Collections Framework and provides dynamic arrays that can grow as needed. Unlike arrays, ArrayLists can change size dynamically when elements are added or removed.

## Conceptual Differences
1. **Size**: Arrays have a fixed size, while ArrayLists can grow and shrink dynamically.
2. **Performance**: Arrays are more efficient in terms of memory usage and performance. ArrayLists have a slight performance overhead due to dynamic resizing.
3. **Flexibility**: ArrayLists provide more functionality and are easier to use when the number of elements can change.

## Example Code
```java
import java.util.ArrayList;

public class DifferenceArraysArrayLists {

    public static void main(String[] args) {
        // Example using an array
        int[] array = new int[5]; // Fixed size array
        array[0] = 10;
        array[1] = 20;
        array[2] = 30;
        array[3] = 40;
        array[4] = 50;
        
        // Uncommenting the next line will cause an ArrayIndexOutOfBoundsException
        // array[5] = 60; // Array has a fixed size and cannot accommodate more elements

        // Printing array elements
        System.out.println("Array elements:");
        for (int i = 0; i < array.length; i++) {
            System.out.println(array[i]);
        }

        // Example using an ArrayList
        ArrayList<Integer> arrayList = new ArrayList<>(); // Dynamic size
        arrayList.add(10);
        arrayList.add(20);
        arrayList.add(30);
        arrayList.add(40);
        arrayList.add(50);
        
        // ArrayList can grow dynamically
        arrayList.add(60); // This works fine
        
        // Printing ArrayList elements
        System.out.println("\nArrayList elements:");
        for (int i = 0; i < arrayList.size(); i++) {
            System.out.println(arrayList.get(i));
        }
    }
}
