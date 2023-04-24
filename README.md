
program1
import java.util.*;

public class Main{
    public static void main(String args[]) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        int[] arr = new int[n];
        
        for (int i = 0; i < n; i++) {
            arr[i] = sc.nextInt();
        }

        int secondLargest = findSecondLargest(arr);
        System.out.println(secondLargest);
    }
    
    static int findSecondLargest(int[] arr)
    {
        int max=Integer.MIN_VALUE;
        int second_max=Integer.MIN_VALUE;
        
        for(int i=0;i<arr.length;i++)
        {
            if(arr[i]>max)
            {
                second_max=max;
                max=arr[i];
            }
            else if(arr[i]>second_max && arr[i]!=max)
            second_max=arr[i];    
        }

        return second_max;
    
    }
}
program2
import java.util.Scanner;

public class Main {
  public static void main(String[] args) {
    Scanner input = new Scanner(System.in);
    String str = input.nextLine();
    System.out.println(reverseString(str));
  }

  public static String reverseString(String str) {
    char ch[]=str.toCharArray();
        String rev="";
           for(int i=ch.length-1;i>=0;i--)
           {
            rev+=ch[i];

           }
           return rev;
  }
}
program3
import java.io.*;
import java.util.Scanner;
class Main{
    public static void main(String[] args){
        Scanner in = new Scanner(System.in);
        int number = in.nextInt();

        System.out.println(factorial(number));
    }

    static int factorial(int number)
    
    {
        

        if(number == 0)
        {
            return 1;

        }
        else if(number == 1){
            return 1;
        }
        else{

        
        return number*factorial(number-1);
       }
       }
    
    }
program4
import java.util.*;

class LinkedList {
    Node head;

    static class Node {
        int data;
        Node next;

        // parametrized constructor
        Node(int data) {
            this.data = data;
            this.next = null;
        }
    }

    void insertTail(int data) {
        Node newNode = new Node(data);

        if (this.head == null) {
            // list is empty
            this.head = newNode;
        } else {
            // list is not empty
            Node thead = this.head;
            while (thead.next != null) {
                thead = thead.next;
            }

            thead.next = newNode;
        }

    }

    void printList() {
        Node thead = this.head; // this -> list
        while (thead != null) {
            System.out.print(thead.data + " -> ");
            thead = thead.next;
        }
    }

    void insertHead(int data) {
        // 1. create a new node
        // create an object to the class
        Node newNode = new Node(data);

        // 2. update the newNode
        // store the address of head to newNode.next
        newNode.next = this.head;

        // 3. change the head
        this.head = newNode;
    }

    /**
     * The function should return the length or number of nodes
     * in the list
     */
    int length() {
        // TODO:
        int count = 0;
        Node current = this.head;
        while (current !=null) {
            count++;
            current = current.next;
        }
        return count;
    }

    int count(int data) {
        // initialize a count variable to
        // to keep track of the number of times data exists
        int nodes = 0;

        Node thead = this.head;

        while (thead != null) {
            if (thead.data == data) {
                nodes++;
            }
            thead = thead.next;
        }

        return nodes;
    }

    public static void main(String[] args) {
        Scanner in = new Scanner(System.in);
        // how to create an object to the class
        LinkedList list = new LinkedList();
        String line = in.nextLine();
        String array[] = line.split("\\s+");
        int numArray[] = new int[array.length];

        for (int i = 0; i < array.length; i++) {
            numArray[i] = Integer.parseInt(array[i]);
        }

        for (int i = 0; i < numArray.length; i++) {
            list.insertHead(numArray[i]);
        }

        System.out.println(list.length());

        // uncomment the following line to print the linked list
        // list.printList();

        in.close();

    }
}
program5
import java.util.*;

class LinkedList {
    Node head;

    static class Node {
        int data;
        Node next;

        // parametrized constructor
        Node(int data) {
            this.data = data;
            this.next = null;
        }
    }

    void insertTail(int data) {
        Node newNode = new Node(data);

        if (this.head == null) {
            // list is empty
            this.head = newNode;
        } else {
            // list is not empty
            Node thead = this.head;
            while (thead.next != null) {
                thead = thead.next;
            }

            thead.next = newNode;
        }

    }

    void printList() {
        Node thead = this.head; // this -> list
        while (thead != null) {
            System.out.print(thead.data + " ");
            thead = thead.next;
        }
    }

    void insertHead(int data) {
        // 1. create a new node
        // create an object to the class
        Node newNode = new Node(data);

        // 2. update the newNode
        // store the address of head to newNode.next
        newNode.next = this.head;

        // 3. change the head
        this.head = newNode;
    }

    
    void deleteTail() {
       if (this.head == null){
        return;
       }
       if (this.head.next == null){
        this.head=null;
        return;
       }
       Node current = this.head;
       while (current.next.next != null){
        current=current.next;
       }
       current.next=null;


        
    }

    int count(int data) {
        // initialize a count variable to
        // to keep track of the number of times data exists
        int nodes = 0;

        Node thead = this.head;

        while (thead != null) {
            if (thead.data == data) {
                nodes++;
            }
            thead = thead.next;
        }

        return nodes;
    }

    public static void main(String[] args) {
        Scanner in = new Scanner(System.in);
        // how to create an object to the class
        LinkedList list = new LinkedList();
        String line = in.nextLine();
        String array[] = line.split("\\s+");
        int numArray[] = new int[array.length];

        for (int i = 0; i < array.length; i++) {
            numArray[i] = Integer.parseInt(array[i]);
        }

        for (int i = 0; i < numArray.length; i++) {
            list.insertHead(numArray[i]);
        }

        list.deleteTail();

        list.printList();

        // uncomment the following line to print the linked list
        // list.printList();

        in.close();

    }
}
program6
import java.util.*;

class LinkedList {
    Node head;

    static class Node {
        int data;
        Node next;

        // parametrized constructor
        Node(int data) {
            this.data = data;
            this.next = null;
        }
    }

    void insertTail(int data) {
        Node newNode = new Node(data);

        if (this.head == null) {
            // list is empty
            this.head = newNode;
        } else {
            // list is not empty
            Node thead = this.head;
            while (thead.next != null) {
                thead = thead.next;
            }

            thead.next = newNode;
        }

    }

    void printList() {
        Node thead = this.head; // this -> list
        while (thead != null) {
            System.out.print(thead.data + " ");
            thead = thead.next;
        }
    }

    void insertHead(int data) {
        // 1. create a new node
        // create an object to the class
        Node newNode = new Node(data);

        // 2. update the newNode
        // store the address of head to newNode.next
        newNode.next = this.head;

        // 3. change the head
        this.head = newNode;
    }

    void insertAtMiddle(int data) {
        Node slow = this.head;
        Node fast = this.head;
        fast = fast.next.next;
        while (fast!=null&&fast.next!=null){
            slow = slow.next;
            fast=fast.next.next;
        }
        Node newNode = new Node(data);
        newNode.next=slow.next;
        slow.next=newNode;
    }

    int count(int data) {
        // initialize a count variable to
        // to keep track of the number of times data exists
        int nodes = 0;

        Node thead = this.head;

        while (thead != null) {
            if (thead.data == data) {
                nodes++;
            }
            thead = thead.next;
        }

        return nodes;
    }

    public static void main(String[] args) {
        Scanner in = new Scanner(System.in);
        // how to create an object to the class
        LinkedList list = new LinkedList();
        String line = in.nextLine();
        String array[] = line.split("\\s+");
        int numArray[] = new int[array.length];
        int middleNode = in.nextInt();

        for (int i = 0; i < array.length; i++) {
            numArray[i] = Integer.parseInt(array[i]);
        }

        for (int i = 0; i < numArray.length; i++) {
            list.insertTail(numArray[i]);
        }

        list.insertAtMiddle(middleNode);

        list.printList();

        // uncomment the following line to print the linked list
        //list.printList();
        list.printList();

        in.close();

    }
}
program7
import java.util.Scanner;

public class StringReverse {
    public static void main(String[] args) 
    {
        Scanner in = new Scanner(System.in);

        // get the input string from the user
        String name = in.nextLine();

        // create an empty stack
        Stack stack = new Stack();

        // traverse through the string from index=0 to name.length() - 1
        
        for(int index=0;index<name.length();index++)
        {
            stack.push(name.charAt(index));
        }
            // for every character at the index,
            // push it to the stack


        // do the following iteratively until the stack becomes empty
        while(!stack.isEmpty())
        {
            System.out.print(stack.tos());
            stack.pop();
        }
            // print the top of the stack

            // pop the stack

        // close the scanner object
        in.close();
    }
}
program8
public class Queue {
    QueueNode front, rear;

    Queue() {
        this.front = null;
        this.rear = null;
    }
    
    // complete the below method
    void enqueue(int data) {
        // create a new node with data
       
        QueueNode newNode=new QueueNode(data);
        // check if the front and rear are equal to null
        if (this.front == null && this.rear == null){
            this.front=newNode;
            this.rear=newNode;
        
            // if true, queue is empty
            // store the reference of newNode to the front and rear pointers
            
        } else {
            this.rear.next=newNode;
            this.rear=newNode;
            // else, queue is not empty
            // unalterred front
            // update the rear pointer alone
            // insert the newNode to the next of rear pointer
        }
        }
    
    

    int getFront() {
        return this.front.data;
    }

    int getRear() {
        return this.rear.data;
    }

    void dequeue() {
        if (this.front != null) {
            this.front = this.front.next;
        }
    }

    public static void main(String[] args) {
        // create an empty queue
        Queue queue = new Queue();

        queue.enqueue(10);
        queue.enqueue(11);
        queue.enqueue(12);
        System.out.println(queue.getFront() + " " + queue.getRear());
    }

}
program9
import java.util.*;
public class SelectionSort {
    public static void main(String[] args) {
        Scanner in = new Scanner(System.in);
        String line = in.nextLine();
        String array[] = line.split("\\s+");
        int numbers[] = new int[array.length];

        for (int i = 0; i < array.length; i++) {
            numbers[i] = Integer.parseInt(array[i]);
        }

        // complete the selection sort logic below
        // run a loop with index -> 0 to numbers.length-2
        for (int i = 0; i < numbers.length-1;i++) {
            int minIndex = i;
            // assume a minimum index -> minIndex
            
            // find the correct minimum index of the minimum value in the numbers array
            // run a loop with j -> index + 1 to numbers.length -1
            for (int j=i+1;j < numbers.length;j++) {
                // check if the numbers[j] is less than numbers[minIndex]
                if (numbers[j]<numbers[minIndex]) {
                    // update the assumed index with the actual minimum index found
                    minIndex = j;
                }
            }

            // we now have our minIndex pointing to the minimum value
            // do a swap with minIndex, index values of numbers array
            int temp = numbers[i];
            numbers[i] = numbers[minIndex];
            numbers[minIndex] = temp;
        }

        // print the array
        for (int i = 0; i < numbers.length; i++) {
            System.out.print(numbers[i] + " ");
        }
    }

}
program10 
import java.util.Scanner;

public class BinarySearch {
    public static void main(String[] args) {
        Scanner in = new Scanner(System.in);
        String line = in.nextLine();
        String array[] = line.split("\\s+");
        int numbers[] = new int[array.length];

        for (int i = 0; i < array.length; i++) {
            numbers[i] = Integer.parseInt(array[i]);
        }

        // get the value to search in the array from the user
        int key = in.nextInt();

        if (doBinarySearch(numbers, key)) {
            System.out.println(key + " found in the array");
        } else {
            System.out.println(key + " not found in the array");
        }

        in.close();
    }

    // complete the doBinarySearch function below
    static boolean doBinarySearch(int numbers[], int key) {
        int left = 0;
        int right = numbers.length-1;
        // set the left and right pointers
        // left pointer to 0 and right pointer to numbers.length - 1

        // do until left > right
        while (left <= right) {
            // calculate the middle element as left + (right - left) / 2
            int middle = left + (right - left) / 2;
            // check if the numbers[middle] is equal to key
            if (numbers[middle] == key) {
                // return true if the condition is true
            return true;
            } 
            // else check if key is less than the numbers[middle]
            else if (key < numbers[middle]) {
                // if true, set the right pointer to middle - 1
                right = middle-1;
            }
            // else check if key is greater than numbers[middle] 
            else {
                // if true, set the left poitner to middle + 1
                left = middle+1;
            }
        }
        // return false otherwise
        return false;
    }
}
