#include<stdio.h>

int main () {


int first, last, middle, size, i, selement, list[100];

printf("enter the element of list:");

scanf("%d",&size);

printf("enter the %d integers in asanding orders:\n",size);

for(i=0;i<size;i++) {
printf("Element %d: ",i+1);
scanf("%d",&list[i]);
}
printf("enter the value to search:");

scanf("%d",&selement);

first=0;

last=size-1;

middle=(first+last)/2;

while(first<last)
{
if(list[middle]<selement)

first=middle+1;

else if(list[middle]==selement) {

printf("element found at index%d\n",middle);
}
else

last=middle-1;

middle=(first+last)/2;
}
if(first>last)
printf("Element not found\n");
}
