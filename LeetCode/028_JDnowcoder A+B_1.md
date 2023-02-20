# 028_JDnowcoder A+B_1

> Author: fengclchn@outlook.com
>
> Date: 02/20/2023

[TOC]

![image-20230220100643926](https://histone-obs.obs.cn-southwest-2.myhuaweicloud.com/noteImg/image-20230220100643926.png)

## 第一次提交

```c++
#include <iostream>
using namespace std;

int main()
{
    int n, m;
    while (cin >> n >> m)
    {
        cout << n + m << endl;
    }
}
```

## 正确答案

```c++
#include <iostream>
using namespace std;

int main() {
    int a, b;
    while (cin >> a >> b) { // 注意 while 处理多个 case
        cout << a + b << endl;
    }
}
// 64 位输出请用 printf("%lld")
```

