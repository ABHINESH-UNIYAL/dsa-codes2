#include<stdio.h>
#define max 5
int stack[max];
int top=-1;
void push(){
    int n;
    if(top==max-1)
    {
        printf("stack overflow\n");
    }
    else
    {
        printf("Enter the value you want to enter\n");
        scanf("%d",&n);
        top=top+1;
        stack[top]=n;
    }
}

void pop(){
    int n;
    if(top==-1)
    {
        printf("stack underflow\n");
    }
    else
    {
        printf(" pooped %d from the stack \n",stack[top]);
        top--;
    }
  }
  void display(){
       int i;
       if(top==-1)
       {
           printf("stack is empty");
       }
       else
       {
           for(i=top;i>=0;i--)
           {
               printf("%d",stack[i]);
           }
           printf("\n");
       }
       
                }
                
int main()
{
    int choice;
    while(1){
            printf("\nMenu\n");
            printf("1.push\n");
            printf("2.pop\n");
            printf("3.display\n");
            printf("4.exit\n");
            printf("Enter your choice");
            scanf("%d",&choice);
            
    switch(choice){
        case 1:push();
               break;
        case 2:pop();
               break;
        case 3:display();
               break;
        case 4:
              printf("Exit...\n");
              exit(0);
              default :
               printf("Invalid choice ! \n");
    }
            
    }
    return 0;
}
    
