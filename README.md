# 2021-AST-Task
This repository is for 2021-AST-Task

```c
#include <stdio.h>
#include <stdlib.h>
typedef struct std{
    int id;
    double grades;
};
void duru(struct std *stu ,int n)
{
    int i;
    for(i=1;i<=n;i++)
    scanf("%d %lf",&stu[i].id,&stu[i].grades);
}
void sort(struct std *stu,int n)
{
    int i,b,c,d,j;
    for(i=1;i<=n;i++)
    {
        b=stu[i].grades;
        d=stu[i].id;
        for(j=i;j<=n;j++)
        {
            if(stu[j].grades<=b)
            {
                b=stu[j].grades;
                c=j;
            }
            else continue;
        }
        stu[c].grades=stu[i].grades;
        stu[i].grades=b;
        stu[c].id=stu[i].id;
        stu[i].id=d;
    }
    for(i=1;i<=n;i++)
    printf("%d %lf\n",stu[i].id,stu[i].grades);
}
int main()
{
    int n;
    struct std stu[5];
    scanf("%d",&n);
    duru(stu,n);
    sort(stu,n);
    return 0;
}
```

rgc 是指命令行输入参数的个数，argv存储了所有的命令行参数。

argc和argv中的arg指的是"参数"。其中，argc为整数，用来统计运行程序时送给main函数的命令行参数的个数（个人理解是主函数中字符串的个数）；argv加上* 与[ ]，成为*argv[ ]，表示字符串数组，用来存放指向字符串参数的指针数组，每个元素指向一个参数。各成员含义如下：
argv[0]指向程序运行的全路径名；
argv[1]指向执行程序后的第一个字符串；
argv[2]指向执行程序名后的第二个字符串；
argv[3]指向执行程序名后的第三个字符串；
argv[argc]为NULL

是网上的一些大佬说的其实自己也不太明白

下来有时间再好好学学。

Git大概差不多会用了一点点，最近活动比较多，加上一元分析学也快期中，下来抽时间再好好学习git。
