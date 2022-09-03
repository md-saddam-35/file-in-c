#include <stdio.h>
#include <stdlib.h>
int main()
{

    FILE *file;
    int num,n,i;

    file = fopen("integer.txt", "w");
    if (file == NULL)
    {
        printf("\nfile is opened");

    }
    printf("\n\tenter enteger valu ");
    scanf("%d", &num);
    putw(num,file);
    fclose(file);
    ////////////////

    file = fopen("integer.txt", "r");
    if(file==NULL)
    {
        printf("file is not opened\n");
        
    }
    n= getw(file);

    printf("\t valu of :%d\n", n);

      fclose(file);

    return 0;
}