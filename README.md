# codesofmine
repo
program 1
import java.util.*;
public classMain{
public static void main(Stringargs[]) {
System.out.println("PROGRAM FOR FINDING THE SECOND HIGHEST NUMBER IN AN 
ARRAY");
System.out.println("ENTER THE SIZE OF THE ARRAY");
Scanner sc = newScanner(System.in);
int n = sc.nextInt();
int[] arr = newint[n];
System.out.println("ENTER THE ELEMENTS OF THE ARRAY");
for (int i = 0; i< n; i++) {
arr[i] = sc.nextInt();
}
int secondLargest = findSecondLargest(arr);
System.out.println("The Second Highest Number is "+ secondLargest);
}
static int findSecondLargest(int[] arr)
{
int max=Integer.MIN_VALUE;
int secondLargest=Integer.MIN_VALUE;
for(int i=0;i<arr.length;i++)
{
if(max<arr[i])
{
secondLargest=max;
max=arr[i];
}
elseif(secondLargest<arr[i])
{
secondLargest=arr[i];
}
}
return(secondLargest);
}
}
program2
importjava.util.Scanner;
publicclassMain {
publicstaticvoidmain(String[] args) {
System.out.println("PROGRAM TO REVERSE A STRING USING RECURSION");
System.out.println("ENTER THE STRING TO BE REVERSED USING RECURSION");
Scannerinput = newScanner(System.in);
Stringstr = input.nextLine();
System.out.println("THE REVERSED STRING IS: " + reverseString(str));
}
publicstaticStringreverseString(Stringstr) {
{
if(str.isEmpty())
returnstr;
returnreverseString(str.substring(1))+str.charAt(0);
}
}
}
program3
importjava.util.*;
classMain{
publicstaticvoidmain(String[] args){
System.out.println("PROGRAM TO FIND THE FACTORIAL OF A GIVEN NUMBER 
USING RECURSION");
System.out.println("ENTER THE NUMBER TO FIND THE FACTORIAL OF A GIVEN 
NUMBER USING RECURSION");
Scannerin = newScanner(System.in);
intnumber = in.nextInt();
System.out.println("FACTORIAL OF A GIVEN NUMBER IS: " + 
factorial(number));
}
staticintfactorial(intnumber){
//factorial program
if(number<=1)
{
return1;
}
else
{
return number*factorial(number-1);
}
}
}
program4
importjava.util.*;
classLinkedList {
Nodehead;
staticclassNode {
intdata;
Nodenext;
// parametrized constructor
Node(intdata) {
this.data = data;
this.next = null;
}
}
voidinsertTail(intdata) {
NodenewNode = newNode(data);
if (this.head == null) {
// list is empty
this.head = newNode;
} else {
// list is not empty
Nodethead = this.head;
while (thead.next != null) {
thead = thead.next;
}
thead.next = newNode;
}
}
void printList() {
Nodethead = this.head; // this -> list
while (thead != null) {
System.out.print(thead.data + " -> ");
thead = thead.next;
}
}
void insertHead(intdata) {
// 1. create a new node
// create an object to the class
NodenewNode = newNode(data);
// 2. update the newNode
16
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
intcount =0;
Nodecurrent =this.head;
while( current !=null)
{
count++;
current =current.next; 
}
return count;
}
int count(intdata) {
// initialize a count variable to
// to keep track of the number of times data exists
Int nodes = 0;
Nodethead = this.head;
while (thead != null) {
if (thead.data == data) {
nodes++;
}
thead = thead.next;
}
return nodes;
}
public static void main(String[] args) {
Scanner in = newScanner(System.in);
// how to create an object to the class
System.out.println("PROGRAM TO FIND THE LENGTH OF THE LINKED LIST");
System.out.println("ENTER THE VALUES TO FIND THE LENTH OF THE LINKED 
LIST");
LinkedListlist = newLinkedList();
Stringline = in.nextLine();
Stringarray[] = line.split("\\s+");
17
intnumArray[] = newint[array.length];
for (inti = 0; i<array.length; i++) {
numArray[i] = Integer.parseInt(array[i]);
}
for (inti = 0; i<numArray.length; i++) {
list.insertHead(numArray[i]);
}
System.out.println("LENGTH OF THE LINKED LIST IS:" + list.length());
// uncomment the following line to print the linked list
// list.printList();
in.close();
}
}
program5
Import java.util.*;
Class LinkedList {
Nodehead;
Static classNode {
intdata;
Nodenext;
// parametrized constructor
Node(intdata) {
this.data = data;
this.next = null;
}
}
Void insertTail(intdata) {
NodenewNode = newNode(data);
if (this.head == null) {
// list is empty
this.head = newNode;
} else {
// list is not empty
Nodethead = this.head;
while (thead.next != null) {
thead = thead.next;
}
thead.next = newNode;
}
}
void printList() {
Nodethead = this.head; // this -> list
while (thead != null) {
System.out.print(thead.data + " ");
thead = thead.next;
}
}
void insertHead(int data) {
// 1. create a new node
// create an object to the class
Node newNode = newNode(data);
21
// 2. update the newNode
// store the address of head to newNode.next
new Node.next = this.head;
// 3. change the head
this.head = newNode;
}
void deleteTail() {
// TODO: Complete this function
if(this.head==null){
return;
}
if(this.head.next==null){
this.head=null;
return;
}
Nodethead=this.head;
while (thead.next.next !=null){
thead=thead.next;
}
thead.next=null;
}
Int count(int data) {
// initialize a count variable to
// to keep track of the number of times data exists
intnodes = 0;
Node thead = this.head;
while (thead != null) {
if (thead.data == data) {
nodes++;
}
thead = thead.next;
}
return nodes;
}
Public static void main(String[] args) {
Scanner in = new Scanner(System.in);
// how to create an object to the class
System.out.println("PROGRAM FOR LINKED LIST DELETION AT TAIL");
System.out.println("ENTER THE VALUES OF LINKED LIST");
22
LinkedListlist = newLinkedList();
String line = in.nextLine();
Stringarray[] = line.split("\\s+");
intnumArray[] = newint[array.length];
for (inti = 0; i<array.length; i++) {
numArray[i] = Integer.parseInt(array[i]);
}
for (inti = 0; i<numArray.length; i++) {
list.insertHead(numArray[i]);
}
System.out.println("Linked List Before Deletion");
list.printList();
System.out.println("\nLinked List After Deletion");
list.deleteTail();
list.printList();
System.out.println("\n");
//ncomment the following line to print the linked list
// list.printList();
in.close();
}
}
program6
mportjava.util.*;
class LinkedList {
Nodehead;
Static classNode {
intdata;
Nodenext;
// parametrized constructor
Node(intdata) {
this.data = data;
this.next = null;
}
}
Void insertTail(intdata) {
Node newNode = newNode(data);
if (this.head == null) {
// list is empty
this.head = newNode;
} else {
// list is not empty
Nodethead = this.head;
while (thead.next != null) {
thead = thead.next;
}
thead.next = newNode;
}
}
void printList() {
Nodethead = this.head; // this -> list
while (thead != null) {
System.out.print(thead.data + " ");
thead = thead.next;
}
}
void insertHead(intdata) {
// 1. create a new node
// create an object to the class
NodenewNode = newNode(data);
// 2. update the newNode
// store the address of head to newNode.next
26
newNode.next = this.head;
// 3. change the head
this.head = newNode;
}
void insertAtMiddle(intdata) {
NodenewNode=newNode(data);
if(head==null)
{
Nodenewnode=newNode(data);
System.out.print("There is no nodes in the Linked List, So Newnode 
is Inserted as Head\n");
}
else
{
Nodeslow=this.head;
Nodefast=this.head;
//fast=fast.next.next;
{
while(fast!=null&&fast.next!=null)
{
slow=slow.next;
fast=fast.next.next;
}
newNode.next=slow.next;
slow.next=newNode;
}
}
}
Int count(intdata) {
// initialize a count variable to
// to keep track of the number of times data exists
intnodes = 0;
Nodethead = this.head;
while (thead != null) {
if (thead.data == data) {
nodes++;
}
thead = thead.next;
}
return nodes;
}
27
Public static void main(Stringargs[]) {
Scannerin = newScanner(System.in);
// how to create an object to the class
System.out.println("PROGRAM FOR LINKED LIST INSERTION AT MIDDLE");
System.out.println("ENTER THE VALUES OF LINKED LIST");
LinkedListlist = newLinkedList();
Stringline = in.nextLine();
Stringarray[] = line.split("\\s+");
intnumArray[] = newint[array.length];
System.out.println("ENTER THE VALUE TO BE INSERTED AT MIDDLE");
intmiddleNode = in.nextInt();
for (inti = 0; i<array.length; i++) {
numArray[i] = Integer.parseInt(array[i]);
}
for (inti = 0; i<numArray.length; i++) {
list.insertTail(numArray[i]);
}
System.out.println("LINKED LIST BEFORE INSERTION");
list.printList();
list.insertAtMiddle(middleNode);
System.out.println("\nLINKED LIST AFTER INSERTION");
list.printList();
System.out.println("\n");
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
