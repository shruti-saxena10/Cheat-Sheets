## 1. Insert a Node at the Front/Beginning of the Linked List

```
public class Node {
    int data;
    Node next;

    Node(int new_data){
        this.data=new_data;
        this.next=null;
    }
}

package org.example;

public class Main{
    //to insert Node
    public static Node insertNodeAtFirst(Node head,int new_data){
        Node newNode=new Node(new_data);
        newNode.next=head;
        //return head
        return newNode;
    }
    //printing the ll using head
    public static void printlist(Node head){
        //start from current node
        Node curr=head;
        while(curr!=null){
            System.out.print(" "+curr.data);
        curr=curr.next;
        }
        System.out.println();
    }

    public static void main(String[] args) {

        Node n=new Node(2);
        n.next=new Node(3);
        n.next.next=new Node(4);
        n.next.next.next=new Node(5);
        System.out.println("Original");
        printlist(n1);
        System.out.println("After");
        int data=1;
        Node n2=insertNode(n1,data);
        printlist(n2);
    }
}


```
<img width="401" alt="image" src="https://github.com/user-attachments/assets/f6955064-8751-4fdd-b093-19cbb06cb43d" />

