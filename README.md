~~~
 Ex-12-IMPLEMENTATION-OF-HEAP-STORAGE-ALLOCATION-STRATEGY
IMPLEMENTATION OF HEAP STORAGE ALLOCATION STRATEGY

 Aim :
To write a program to implement heap storage allocation strategy.

ALGORITHM
1. Start the program.
2. Define a function create( ) to create a list of allocated node. This function returns a pointer to head of list.
3. Define a function display(node) to display the list of allocated nodes.
4. Define a function search(node,key) to search for the element in list.
5. Define a function insert(node) to insert element into the list.
6. Stop the program.

 PROGRAM
#include <stdio.h>
#include <stdlib.h>
#define TRUE 1
#define FALSE 0
// Function prototypes
node *create();
void display(node *);
node *search(node *, int);
node *insert(node *);
void insert_after(node *);
// Function definitions
void dele(node **head) {
    int key;
    node *temp = *head;
    node *prev = NULL;
 printf("\nEnter the element you want to delete: ");
    scanf("%d", &key);
 if (prev->next != NULL) {
                temp = prev->next;
                prev->next = temp->next;
                free(temp);
            } else
                printf("\nThe element is not found in the list\n");
        }
    }node *get_node() {
    node *temp = (node *)malloc(sizeof(node));
    if (temp == NULL) {
        printf("\nMemory allocation failed\n");
        exit(1);
    }
    temp->next = NULL;
    return temp;
}
node *create() {
    node *temp, *New, *head = NULL;
    int val;
    char ans = 'y';
    int flag = TRUE
        New = get_node();
        if (New == NULL) {
            printf("\nMemory allocation failed\n");
            exit(1);
        }New->data = val;
        New->next = NULL;

        if (flag == TRUE) {
            head = New;
            temp = head;
            flag = FALSE;
        } else {
            temp->next = New;
            temp = New;
        }printf("\nDo you want to enter more elements? (y/n): ");
        scanf(" %c", &ans);
    } while (ans == 'y' || ans == 'Y');

    printf("\nThe list is created\n");
    return head;
}void display(node *head) {
    node *temp = head;

    if (temp == NULL) {
        printf("\nThe list is empty\n");
        return;
    }
 printf("\n");
    while (temp != NULL) {
        printf("%d ", temp->data);
        if (temp->next != NULL)
            printf("-> ");
        temp = temp->next;
    }
    printf("\n");
}
node *search(node *head, int key) {
    node *temp = head;

    if (temp == NULL) {
        printf("\nThe linked list is empty\n");
        return NULL;
    }while (temp != NULL) {
        if (temp->data == key) {
            printf("\nThe element is present in the list\nThe element is Deleted");
            return temp;
        }
        temp = temp->next;
    }node *insert(node *head) {
    int choice;
    head = insert_head(head);
    head = insert_last(head);
    insert_after(head);
    return head;
}
return New;
}
node *insert_last(node *head) {
    int val;
    node *New = get_node();
    node *temp = head;
    New->next = NULL;
if (head == NULL)
        head = New;
    else {
        while (temp->next != NULL)
            temp = temp->next;
        temp->next = New;
    } return head;
}void insert_after(node *head) {
    int key;
    node *New = get_node();
    node *temp = head;

    printf("\nEnter the element after which you want to insert the node: ");
    scanf("%d", &key);
 while (temp != NULL) {
        if (temp->data == key) {
            printf("\nEnter the element you want to insert: ");
            scanf("%d", &New->data);
            New->next = temp->next;
            temp->next = New;
            return;
        }
        temp = temp->next;
    }
int main() {
    int choice;
    node *head = NULL;
do {
        printf("\nProgram to perform various operations on heap using dynamic memory management\n");
        printf("1. Create\n");
        printf("2. Display\n");
        scanf("%d", &choice);
        switch (choice) {
            case 1:
                head = create();
                break;
            case 2:
                display(head);
                break;
            case 3:
                head = insert(head);
                break;
            default:
                printf("Invalid choice, try again.\n")
    } while (choice != 5);
 return 0;
}
~~~

# OUTPUT
![image](https://github.com/niranjanadevi-s/Ex-12-IMPLEMENTATION-OF-HEAP-STORAGE-ALLOCATION-STRATEGY/assets/141748873/f93e2763-93b7-4862-887b-02a40dbc0ab1)

![image](https://github.com/niranjanadevi-s/Ex-12-IMPLEMENTATION-OF-HEAP-STORAGE-ALLOCATION-STRATEGY/assets/141748873/ca705f3d-2b3b-4a78-aa9b-02c5e9a21ac2)

![image](https://github.com/niranjanadevi-s/Ex-12-IMPLEMENTATION-OF-HEAP-STORAGE-ALLOCATION-STRATEGY/assets/141748873/4d1c8ab6-ce0b-4b74-aaf7-f657f361db1a)

# RESULT
The heap storage allocation strategy is implemented successfully, and the output is 
verified.
