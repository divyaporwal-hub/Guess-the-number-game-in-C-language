# Guess-the-number-game-in-C-language
#include<stdio.h>
#include<stdlib.h>
#include<time.h>
int main()
{
    int n, guess,nog=1;
    
    srand(time(0));
    n=rand()/100000000+1;
    
    //printf("The random no is: %d\n",n);
    do{
    printf("Guess the number between 1 and 100:\n");
    scanf("%d",&guess);
    
        if(n<guess){
            printf("Lower number please**\n");
        }
        else if(n>guess){
            printf("Higher number please**!!\n");
        }
        else if(n==guess)
        {printf("U guess correct in %d attempts!!",nog);}
        nog++;
    }while(n!=guess);
    return 0;
}
