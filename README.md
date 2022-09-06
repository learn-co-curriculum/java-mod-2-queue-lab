# Queue Lab

## Learning Goals

- Use a queue to keep track of information.

## Instructions

Create a lightweight, simplified, restaurant reservation system.

Follow the given instructions:

1. The restaurant has 2 tables.
2. In an input loop, ask the user if they want to check someone in or check
   someone out.
3. If they want to check someone in, check if a table is available.
   1. If a table is available, check them in.
   2. If a table is not available, put them on a waiting list.
4. If they want to check someone out:
   1. Free one of the tables.
   2. Immediately assign the table to the next person on the waiting list.

## Hints

1. You can use an array, a list, a map or a queue for your tables - each data
   structure has pros and cons, but you can make each one work for the list of
   tables.
2. Use a queue for your wait list, as that's the most natural data structure for
   this type of scenario.
3. The `Restaurant` class should have both the table list and the wait list.
4. The `Restaurant` class will have a method you might call `checkin()` and a
   method called `checkout()` that will be responsible for implementing the logic
   we described above.

## Starter Code

Consider the starter code in the driver class. Note that the driver class is not
finished. You will need to write the `main()` method to prompt the user:

```java
public class RestaurantDriver {
    public static void main(String[] args) {
        // Your code here
    }

    public static void printMenu() {
        System.out.println("Welcome to the Restaurant! What would you like to do?");
        System.out.println("0. Exit");
        System.out.println("1. Check in");
        System.out.println("2. Check out");
        System.out.println();
    }
}
```

### Sample Output

Here is an example run of the code for your reference. Make sure your output
looks the same when given these values:

```plaintext
Welcome to the Restaurant! What would you like to do?
0. Exit
1. Check in
2. Check out

1
What is the name you want to check in?
Leslie
Leslie has been checked in and sat at table 1

Welcome to the Restaurant! What would you like to do?
0. Exit
1. Check in
2. Check out

1
What is the name you want to check in?
Ron
Ron has been checked in and sat at table 2

Welcome to the Restaurant! What would you like to do?
0. Exit
1. Check in
2. Check out

2
The table has been cleared!
There is no one currently waiting - table will remain available.

Welcome to the Restaurant! What would you like to do?
0. Exit
1. Check in
2. Check out

1
What is the name you want to check in?
Ann
Ann has been checked in and sat at table 1

Welcome to the Restaurant! What would you like to do?
0. Exit
1. Check in
2. Check out

1
What is the name you want to check in?
Tom
Tom has been added to the wait list.

Welcome to the Restaurant! What would you like to do?
0. Exit
1. Check in
2. Check out

1
What is the name you want to check in?
April
April has been added to the wait list.

Welcome to the Restaurant! What would you like to do?
0. Exit
1. Check in
2. Check out

1
What is the name you want to check in?
Andy
Andy has been added to the wait list.

Welcome to the Restaurant! What would you like to do?
0. Exit
1. Check in
2. Check out

2
The table has been cleared!
Tom has been seated from the wait list!

Welcome to the Restaurant! What would you like to do?
0. Exit
1. Check in
2. Check out

2
The table has been cleared!
April has been seated from the wait list!

Welcome to the Restaurant! What would you like to do?
0. Exit
1. Check in
2. Check out

2
The table has been cleared!
Andy has been seated from the wait list!

Welcome to the Restaurant! What would you like to do?
0. Exit
1. Check in
2. Check out

2
The table has been cleared!
There is no one currently waiting - table will remain available.

Welcome to the Restaurant! What would you like to do?
0. Exit
1. Check in
2. Check out

2
The table has been cleared!
There is no one currently waiting - table will remain available.

Welcome to the Restaurant! What would you like to do?
0. Exit
1. Check in
2. Check out

2
There is no one to checkout - all tables are available

Welcome to the Restaurant! What would you like to do?
0. Exit
1. Check in
2. Check out

0

```
