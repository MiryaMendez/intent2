# intent2
uu
#include <stdio.h>
#include <stdlib.h>
void recorrematriz(int M[][4]) 
{
    int i, j;
    for (i=0; i<4; i++) 
	{
        for (j=0; j<4; j++) 
		{
            M[i][j]++;
        }
    }
}
void invertirarreglo(int M[][4]) 
{
    int i, j;
    for (i=0; i<4; i++)
	 {
        for (j=0; j<4; j++)
		 {
            M[i][j] = 255 - M[i][j];
         }
    }
}
int main() 
{
    int i,j; 
    int imagen[4][4]=
    {
         {255, 255, 255, 255},
        {255, 127, 127, 127},
        {255, 0, 127, 255},
        {0, 0, 255, 255}     
    };
    recorrematriz(imagen);
    printf("la matriz original es:\n");
    for(i=0; i<4; i++) 
	{
        for(j=0; j<4; j++) 
		{
            printf("%d ", imagen[i][j]);
        }
        printf("\n");
    }
invertirarreglo(imagen);
    printf("Matriz invertida:\n");
    for (i=0; i<4; i++) 
	{
        for(j=0; j<4; j++)
		{
            printf("%d ", imagen[i][j]);
        }
        printf("\n");
    }
    return 0;
}
