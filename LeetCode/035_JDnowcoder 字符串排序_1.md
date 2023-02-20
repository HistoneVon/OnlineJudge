# 035_JDnowcoder 字符串排序_1

> Author: fengclchn@outlook.com
>
> Date: 02/20/2023

[TOC]

![image-20230220173540986](https://histone-obs.obs.cn-southwest-2.myhuaweicloud.com/noteImg/image-20230220173540986.png)

## 第一次提交

```c++
#include <string>
#include <iostream>
#include <vector>
#include <algorithm>
using namespace std;

int main()
{
    int n;
    string str;
    vector<string> arr;
    cin >> n;
    for (int i = 0; i < n; ++i)
    {
        cin >> str;
        arr.push_back(str);
    }
    sort(arr.begin(), arr.end());
    for (int i = 0; i < arr.size(); ++i)
    {
        cout << arr[i] << " ";
    }
}
```

