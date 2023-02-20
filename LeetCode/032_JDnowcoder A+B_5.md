# 032_JDnowcoder A+B_5

> Author: fengclchn@outlook.com
>
> Date: 02/20/2023

[TOC]

![image-20230220112737807](https://histone-obs.obs.cn-southwest-2.myhuaweicloud.com/noteImg/image-20230220112737807.png)

## 第一次提交

```c++
#include <iostream>
using namespace std;

int main()
{
    int t, n, m;
    int sum;
    cin >> t;
    for (int i = 0; i < t; ++i)
    {
        while (cin >> n)
        {
            sum = 0;
            for (int j = 0; j < n; ++j)
            {
                cin >> m;
                sum += m;
            }
            cout << sum << endl;
        }
    }
    return 0;
}
```

