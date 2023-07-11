# C-p45-2-
C语言学习笔记 p45 作业讲解(2)

#include<stdio.h>
struct stu
{
    int num;
    char name[10];
    int age;
};

void fun(struct stu* p)
{
    printf("%s\n",(*p).name);
    return;
}
int main()
{
    structnstunstudents[3]={{9801,"zhang",20},{9802,"wang",19},{9803,"zhao",18}};
    fun(students+1);
    return 0;
}//输出“wang”

int main()
{
    int money=0;
    int total=0;
    int empty=0;
    scanf("%d",&money);
    //买回来的汽水喝掉
    total=money;
    empty=money;
    //换回来的汽水
    while(empty>=2)
    {
        total+=empty/2;
        empty=empty/2+empty%2;
    }
    printf("total=%d\n";total);
    return 0;
}


void print(int arr[],int sz)
{
    int i=0;
    for(i=0;i<sz;i++)
    {
        printf("%d",arr[i]);
    }
    printf("\n");
}

void move(int arr[],int sz)
{
    int left=0;
    int right=sz-1;
   while(left<right)
  {
    //从左边找偶书
    while((left<right)&&(arr[left]%2==1))
    {
        left++
    }
    //从右边找奇数
    while((left<right)&&(arr[right]%2==0))
    {
        right--;
    }
    if(left<right)
    {
        int tmp=arr[left];
        arr[left]=arr[right];
        arr[right]=tmp;
    }
  }
}
int main()
{
    int arr[]={1,2,3,4,5,6,7,8,9,10};
    int sz=sizeof(arr)/sizeof(arr[0]);
    move(arr,sz);
    print(arr,sz);
    return 0;
}
