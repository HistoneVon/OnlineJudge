# 034_JDnowcoder A+B_7

> Author: fengclchn@outlook.com
>
> Date: 02/20/2023

[TOC]

![image-20230220165648140](https://histone-obs.obs.cn-southwest-2.myhuaweicloud.com/noteImg/image-20230220165648140.png)

## 第一次提交

```c++
#include <iostream>
using namespace std;

int main()
{
    int m;
    int sum = 0;
    while (cin >> m)
    {
        sum += m;
        if (cin.get() == '\n')
        {
            cout << sum << endl;
            sum = 0;
        }
    }

    return 0;
}
```

