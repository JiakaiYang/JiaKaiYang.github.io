---
title: C语言中malloc函数的应用
author: Kiah
top: true
hide: false
cover: false
toc: true
mathjax: false
categories: C语言
tags:
  - 动态分配内存
keywords: malloc
reprintPolicy: cc_by
date: 2022-02-06 20:30:51
summary: 想要更加灵活运用c语言必须掌握的知识点。理解它，能熟练运用它，让你的编程水平进一步提升。
---
## 传统数组的缺点

1.数组长度必须事先定制，且只能是常数，不能是变量。

2.传统形式定义的数组，该数组的内存程序员无法手动释放。数组一旦定义，系统为该数组分配存储空间就会一直存在，除非数组所在的函数运行结束,数组的空间才会被自动释放.

3.数组的长度不能在运行的过程中动态的扩充或者减小。（数组的长度一旦定义就不能再改变。）

4.a函数定义的数组，在a函数运行期间可以被其他函数运用，但是a函数运行完毕后，a函数中的数组无法被其他函数运用。

## 动态分配内存就能很好解决传统数组的缺点。

### 使用方法

要使用malloc函数必须引入头文件#include <malloc.h>

malloc函数只有一个形参

```c
#include <stdio.h>
#include <malloc.h>
int main(void)
{
    int i = 5; //系统默认为i开辟4个字节的空间来存放整型变量  
    int * p = (int *) malloc(4);//4表示请求系统为本程序分配4个字节的空间
    /**
     * 因为 malloc 只返回 分配好的空间  并不会指定 该内存被哪种类型的数据使用
     * 所以 加上(int *) 强制类型转换，表示 该地址用来存储int类型的数据。
     * 
     */
    scanf("%d",p);
    printf("%d\n",*p);
    free(p);//p指针是由系统自动分配的空间无法释放，但是释放了p指向的空间。
    return 0;
}
```



## 用malloc动态分配空间的方式创建数组

#### 代码演示

```c
#include <stdio.h>
#include <malloc.h>

void printArr(int *,int); //声明一个打印数组的函数
int main(void)
{
    int arr[5]; // 如果int 占 4个字节的话，那么数组arr占20字节
    int len;
    int *pArr;
    printf("请输入数组长度：");
    scanf("%d", &len);
    pArr = (int *)malloc(sizeof(int) * len); //动态分配内存 大小为 int类型所占字节的 len 倍
    printf("请输入%d个int类型的数值:\n",len);
    for (int i = 0; i < len; i++)
    {
        scanf("%d",&pArr[i]);  //输入int 类型的数值
    }
    printArr(pArr,len); //打印数组
    //用完数组之后释放空间
    free(pArr);
    return 0;
}
void printArr(int * pArr,int len)//打印方法的实现
{
     printf("数组打印结果为:");
    for(int i = 0; i <len;i++)
    {
        printf("%d  ",pArr[i]);
    }
    printf("\n");
}
```



## 函数之间运用malloc创建的数组

#### 代码展示(比较传统创建方式第4点缺点)

```c
#include <stdio.h>
#include <malloc.h>
int * f();
int * c();
void b(int * pArr);
int main(void)
{
    int * arr = f();
    b(arr);
    free(arr);

    // int * arr2 = c();   这里会出现一个警告    函数c() 返回局部变量的地址
    // b(arr2);
    return 0;
}
void b(int * pArr)
{
  printf("%d\n",pArr[2]);
}

int * f()
{
    int * pArr = (int*)malloc(sizeof(int) * 5);
    for (int i = 0; i < 5; i++)
    {
        pArr[i] = i + 2;
    }
    return pArr;
}
int * c()
{
    int arr[5];
    for (int i = 0; i < 5; i++)
    {
        arr[i] = i + 2;
    }
    return arr;
}
```

