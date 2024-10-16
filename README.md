# Exp-18

## Aim:
To implement a stack data structure using an array in C++ and perform basic stack operations such as push, pop, peak, and display.

## Software Used:
- Dev c++

## Theory:
A stack is a linear data structure that follows the Last In, First Out (LIFO) principle. It has two main operations: push (to add an element to the top) and pop (to remove the top element). Other operations include peak (to access the top element without removing it) and display (to show the current elements in the stack). Stacks are used in various applications such as expression evaluation, function call management, and undo mechanisms. The program simulates a stack using an array with a fixed size.

## Program 1: Stack Implementation.
<strong> Code: </strong>
<br>
```cpp
// Premish Ninawe
// 23070123092
// ENTC B1
#include <iostream>
using namespace std;
#define size 5
#define ERROR -9999
class Stack{
    int top, ar[size];
    public:
    Stack()
    {
        top=-1;
        ar[0]=0;
    }
    void push(int);
    int pop();
    int peak();
    void disp();
};
void Stack::push(int num)
{
    if (top==size-1)
    {
        cout<<"STACK OVERFLOW: Stack is full"<<endl;
        return;
    }
    else
    {
        ar[++top]=num;
    }
}
int Stack::pop()
{
    int val;
    if(top==-1)
    {
        cout<<"STACK UNDERFLOW: STACK IS EMPTY"<<endl;
        return ERROR;
    }
    else{
         val=ar[top--];
         return val;
    }
}
int Stack::peak()
{
    if(top==-1)
    {
        cout<<"STACK UNDERFLOW: stack is empty"<<endl;
        return ERROR;
    }
    else
    {
        return ar[top];
    }
}
void Stack::disp()
{
    if(top==-1)
    {
       cout<<"STACK UNDERFLOW: stack is empty"<<endl;
        return ;
    }
    else
    {
        int i=0;
        while(i!=(top+1))
        {
            cout<<ar[i]<<"  ";
            i++;
        }
    }
}
int main()
{
    Stack s1;
    s1.push(7);
    s1.push(10);
    s1.push(4);
    int val=s1.pop();
    cout<<val;
    int top=s1.peak();
    cout<<top;
    s1.disp();
    return 0;
}

```
<strong> Output: </strong>
<br>
![image](https://github.com/user-attachments/assets/3e9a0b62-3d07-4855-9844-7bd082fa5a70)


## Conclusion:
In this program, a stack is implemented using a fixed-size array. Operations such as push, pop, peak, and display are successfully performed. The program handles overflow and underflow conditions, displaying appropriate error messages when the stack is full or empty. This program demonstrates the essential working of the stack data structure.
