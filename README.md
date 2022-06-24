# my-problem
/*水仙花数是指一个N位正整数（N>=3)，它的每个位上的数字的N次幂之和等于它本身。
要求编写程序，计算所有的N位水仙花数。
输入在一行中给出一个正整数N（3<=N<=7)。
按递增顺序输出所有N位水仙花数，每个数字占一行。
*/
#include<stdio.h>
int main(){
    
    int n;
    printf("请输入一个正整数：");
    scanf("%d",&n);
    int i;
    int z=1;
    int b;
    int sum=0;
    int c;
    
    for(i=1;i<n;i++){
        z*=10;
    }
    i=z;
    while(i<z*10){
        c=i;
        while(c>0){
            b=c%10;
            int s=1;
            int p=b;
            while(s<n){
                p*=b;
                s++;
            }
            sum+=p;
            c/=10;
        }
        if(sum==i){
            printf("%d\n",i);
        }i++;
    }
    return 0;
}
