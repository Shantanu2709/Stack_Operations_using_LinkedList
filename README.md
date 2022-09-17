# Stack_Operations_using_LinkedList
Operations in Stack data structure like push, pop, peek using Linked_List...
class StackB {
    static class Node 
    {
        int data;
        Node next;
        Node (int data)
        {
            this.data=data;
            this.next=null;
        }
    }
   public static class stack
    {
    static Node head=null;
    static boolean isEmpty()
    {
        return head==null;
    }
    static void push(int data)
    {
        Node newNode = new Node(data);
        if(isEmpty())
        {
            head=newNode;
            return;
        }
        newNode.next=head;
        head=newNode;
    }
    static int pop()
    {
        if(isEmpty())
        {
            return -1;
        }
        int top=head.data;
        head=head.next;
        return top;
         }
         static int peek()
         {
             if(isEmpty())
             {
                 return -1;
             }
             return head.data;
         }
    }
    public static void main(String[] args) 
    {
       stack ss = new stack();
       ss.push(1);
       ss.push(2);
       ss.push(3);
       while(!ss.isEmpty())
       {
           System.out.println(ss.peek());
           ss.pop();
       }
    }
}
