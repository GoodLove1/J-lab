# J-lab


```

class Stack{

private int arr[];

private int top;

private int capacity;

Stack(int size){

arr = new int[size];

capacity = size;

top = -1;

}

public void push(int x)

{

if(isFull())

{

System.out.println("Overflow\nProgram Terminated\n");

System.exit(-1);

}

System.out.println("Inserting " + x);

arr[++top] = x;

}

public int pop()

{

if (isEmpty())

{

System.out.println("Underflow\nProgram Terminated");

System.exit(-1);

}

System.out.println("Removing " + peek());

return arr[top--];

}

public int peek()

{

if (!isEmpty()) {

return arr[top];

}

else {

System.exit(-1);

}

return -1;

}

public int size() {

return top + 1;

}

public boolean isEmpty() {

return top == -1;

}

public boolean isFull() {

return top == capacity - 1;

}}

class Main1

{

public static void main (String[] args)

{

Stack stack = new Stack(3);

stack.push(1);

stack.push(2);

stack.pop();

stack.pop();

stack.push(3);

System.out.println("The top element is " + stack.peek());

System.out.println("The stack size is " + stack.size());

stack.pop();

if (stack.isEmpty()) {

System.out.println("The stack is empty");

}

else {

System.out.println("The stack is not empty");

}}}

```

# queue

```

import java.io.*;

import java.util.*;

import java.lang.*;

class Queue

{

private int[]arr;

private int front;

private int rear;

private int capacity;

private int count;

Queue(int size)

{

arr=new int[size];

capacity=size;

front=0;

rear=-1;

count=0;

}

public int dequeue()

{

if(isEmpty())

{

System.out.println("Underflow\nProgram Terminated");

System.exit(-1);

}

int x=arr[front];

System.out.println("Removing"+ x);

front=(front + 1)% capacity;

count--;

return x;

}

public void enqueue(int item)

{

if(isFull())

{

System.out.println("Overflow\nProgram Terminated");

System.exit(-1);

}

System.out.println("inserting"+ item);

rear=(rear + 1)% capacity;

arr[rear]=item;

count++;

}

public int peek()

{

if(isEmpty())

{

System.out.println("Underflow\nprogramTerminated");

System.exit(-1);

}

return arr[front];

}

public int size()

{

return count;

}

public boolean isEmpty()

{

return(size()==0);

}

public boolean isFull()

{

return(size()==capacity);

}}

class Main1

{

public static void main(String args[])

{

Queue q= new Queue(5);

q.enqueue(1);

q.enqueue(2);

q.enqueue(3);

System.out.println("The front element is"+q.peek());

q.dequeue();

System.out.println("The front element is"+q.peek());

System.out.println("The queue size is"+q.size());

q.dequeue();

q.dequeue();

if(q.isEmpty()){

System.out.println("The Queue is empty");}

else{

System.out.println("The queue is not empty");

}}}


```
