# yash_print_linkedlist.c
#include<stdio.h>
#include<stdlib.h>
#include<conio.h>
struct node
{
	int value;
	struct node *next;
};
void printLinkedlist(struct node *q)

{
	struct node *p;
	p=q;
	while(p!=NULL)
	{
		printf("%d  ",p->value);
		p=p->next;
	}
}
void main()
{

	struct node *head;
	struct node *one;
	struct node *two;
	struct node *three;
	struct node *four;
	clrscr();
	head=(struct node *)malloc(sizeof(struct node));
	one=(struct node *)malloc(sizeof(struct node));
	two=(struct node *)malloc(sizeof(struct node));
	three=(struct node *)malloc(sizeof(struct node));
	four=(struct node *)malloc(sizeof(struct node));
	head->value=10;
	one->value=1;
	two->value=2;
	three->value=3;
	four->value=4;
	head->next=one;
	one->next=two;
	two->next=three;
	three->next=four;
	four->next=NULL;
	printLinkedlist(head);
	getch();
}


