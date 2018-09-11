#include<stdio.h>
#include<stdlib.h>
typedef struct node
{
	int coe;
	int man;
	struct node *next;
}NODE;
typedef struct poly
{
	NODE *st;
}POLY;
void init(POLY *t)
{
	t->st=NULL;
}
NODE *creteNode(int c,int m)
{
	NODE *a=(NODE *)malloc(sizeof(NODE));
	a->coe=c;
	a->man=m;
	a->next=NULL;
	return a;
}
void delpoly(POLY *t)
{
	NODE *a=t->st;
	while(t->st!=NULL)
	{
	  t->st=a->next;
	  free(a);
	  a=t->st;
	}
}
void cretepoly(POLY *p)
{
	NODE *a,*b;
	int c,m;
	delpoly(p);
	while(1)
	{
	  printf("\n coeman");
	  scanf("%d%d",&c,&m);
	  if(c==0&&m==0)
	       break;
	  if(p->st==NULL)
	  	p->st=b=createNode(c,m);
	  else
	  {
	    if(m>=b->man)
	       printf("\n invalid");
	    else
	    {
	       a=createNode(c,m);
	       b->next=a;
	       b=a;
	     }
	  }
	}	
}
void displaypoly(POLY *p)
{
	NODE *a=p->st;
	if(a==NULL)
	   printf("\n empty list");
	else
	{
	   printf("\n poly");
	   while(a!=NULL)
	   {
		if(a->coe>0)
	           printf("\n +");
	        printf("%d %d",a->coe,a->man);
		a=a->next;
	   }
	 }
}
POLY add(POLY *p,POLY *q)
{
	POLY r;
	NODE *a=p->st,*b=q->st,*c,*d;
	int co,ma;
	init(&r);
	if(a==NULL||b==NULL)
	   return r;
	while(a&&b)
	{
	  if(a->man==b->man)
	  {
	    co=a->coe+b->coe;
	    ma=a->man;
	    a=a->next;
	    b=b->next;
	  }
	else
	{
	  if(a->man>b->man)
	  {
	    co=a->coe;
	    ma=a->man;
	    a=a->next;
	  }
	  else	
	  {
	     co=b->coe;
	     ma=b->man;
	     b=b->next;
	   }
	 }
	if(r.st==NULL)
	  r.st=d=createNode(co,ma);
	else
        {
	   c=createNode(co,ma);
	   d->next=c;
	   d=c;
         }
        }
	while(a)
	{
          co=a->coe;
	  ma=a->man;
	  c=createNode(co,ma);
	  d->next=c;
	  d=c;
	  a=a->next;
	 }
	 while(b)
	 {
            co=b->coe;
	    ma=b->man;
	    c=creteNode(co,ma);
	    d->next=c;
	    d=c;
	    b=b->next;
	  }
	  return r;
}
int main()
{	
	int opt,d;
	POLY p;
	while(1)
	{
 	  printf("\n polynomial expression\n menu\n1.createpoly\n2.createpoly\n3.display\n4.display\n5.addpoly\n6.display\noption");
	  scanf("%d",&opt);
	  if(opt>6)
            break;
	  switch(opt)
	  {
	  case 1:
	  createpoly(&p);
	  break;
          case 2:
	  createpoly(&p);
	  break;
	  case 3:
	  display(&p);
	  break;
	  case 4:
	  display(&p);
	  break;
	  case 5:
	  addpoly(&p);
	  break;
	  case 6:
	  display(&p);
	  break;
	  }
	 }
} 
	  
