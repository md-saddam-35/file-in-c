#include<stdio.h>
int main(){




FILE *file;

char name[200];
printf("Enter your full name :");
gets(name);
int length = strlen(name);


  file=fopen("test.txt","w");

if (file==NULL)
{
    printf("file doesn't exist");
}

else
{
int i;
printf("file is opened\n");
for ( i = 0; i <length; i++)
{
    fputc(name[i],file);
}
printf("file is writing succsefully");

fclose(file);
}
//medle time
int n;
  file=fopen("test.txt","r");

if (file==NULL)
{
    printf("file doesn't exist");
}
else{

for (int  i = 0; i <length; i++)
{
    n =fgetc(name[i]);
    printf("%c",n);
}




}





    getch();
}