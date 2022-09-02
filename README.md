# life-story

#include<stdio.h>
int main(){

FILE *file;
char fch[100];
char lch[100];
int h;
file = fopen("test1.txt","r");

if (file == NULL)
{
    printf("file not opened");
}
else{
    printf("file is opened\n");

  fscanf(file,"%s\t %s\t",&fch,&lch)  ;
  printf("%s %s\n",fch,lch);

fclose(file);
}



getch();
}
