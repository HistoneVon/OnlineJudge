# 036_JDnowcoder 字符串排序_2

> Author: fengclchn@outlook.com
>
> Date: 02/20/2023

[TOC]

![image-20230220205131858](https://histone-obs.obs.cn-southwest-2.myhuaweicloud.com/noteImg/image-20230220205131858.png)

## 第一次提交

```c++
#include <string>
#include <vector>
#include <iostream>
#include <algorithm>
using namespace std;

int main()
{
    string str;
    vector<string> arr;
    while (cin >> str)
    {
        arr.push_back(str);
        if (cin.get() == '\n')
        {
            sort(arr.begin(), arr.end());
            for (int i = 0; i < arr.size(); ++i)
            {
                cout << arr[i] << " ";
            }
            cout << endl;
            vector<string>().swap(arr);
        }
    }
    return 0;
}
```

