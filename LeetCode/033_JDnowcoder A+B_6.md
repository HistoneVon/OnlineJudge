# 033_JDnowcoder A+B_6

> Author: fengclchn@outlook.com
>
> Date: 02/20/2023

[TOC]

![image-20230220113945697](https://histone-obs.obs.cn-southwest-2.myhuaweicloud.com/noteImg/image-20230220113945697.png)

## 第一次提交

```c++
#include <iostream>
using namespace std;

int main()
{
    int n, m;
    int sum;
    while (cin >> n)
    {
        sum = 0;
        for (int i = 0; i < n; ++i)
        {
            cin >> m;
            sum += m;
        }
        cout << sum << endl;
    }

    return 0;
}
```

