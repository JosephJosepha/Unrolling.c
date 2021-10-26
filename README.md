# Unrolling.c

Write a C program to perform loop unrolling

 #include<stdio.h>
//#include<conio.h>
void main()
{
unsigned int n;
int x;
char ch;
//clrscr();
printf("\nEnter N\n");
scanf("%u",&n);
printf("\n1. Loop Roll\n2. Loop UnRoll\n");
printf("\nEnter ur choice\n");
int countbitx(unsigned int n)
{
    int bits = 0,i=0;
    while (n != 0)
    {
 if (n & 1) bits++;
 n >>= 1;
 i++;
    }
    printf("\n no of iterations  %d",i);
    return bits;
}
int countbity(unsigned int n)
{
    int bits = 0,i=0;
    while (n != 0)
    {
 if (n & 1) bits++;
 if (n & 2) bits++;
 if (n & 4) bits++;
 if (n & 8) bits++;
 n >>= 4;
 i++;
    }
    printf("\n no of iterations  %d",i);
    return bits;
} 
scanf(" %c",&ch);
switch(ch)
{
case '1':
  x=countbitx(n);
  printf("\nLoop Roll: Count of  1's    :  %d" ,x);
  break;
case '2':
  x=countbity(n);
  printf("\nLoop UnRoll:  Count of 1's  :  %d" ,x);
  break;
default:
  printf("\n Wrong Choice\n");

}
//getch();
}
