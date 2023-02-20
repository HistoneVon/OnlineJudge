# 030_JDnowcoder A+B_3

> Author: fengclchn@outlook.com
>
> Date: 02/20/2023

[TOC]

![image-20230220102340047](https://histone-obs.obs.cn-southwest-2.myhuaweicloud.com/noteImg/image-20230220102340047.png)

## 第一次提交

```c++
#include <iostream>
using namespace std;

int main() {
    int n, m;
    while (cin >> n >>m) {
        if (n == 0 && m == 0) {
            break;
        } else {
            cout << n + m << endl;
        }
    }
    return 0;
}
```

