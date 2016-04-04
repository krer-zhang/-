#include<stdio.h>
#include<stdlib.h>
void main()
{
        float n;
        FILE *p;
        printf("请输入需要写入 的数字\n");

        if((p=fopen("实验三_1.dat","w"))==NULL)
        {
                printf("无法打开此文件\n");
                exit(0);
        }
        scanf("%f",&n);
        while(n!=-1)
        {
                scanf("%f",&n);
                fprintf(p,"%f",n);
                fprintf(p,"\n");
        }
                fclose(p);
                exit(0);
}
