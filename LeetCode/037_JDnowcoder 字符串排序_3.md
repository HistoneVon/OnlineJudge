# 037_JDnowcoder 字符串排序_3

> Author: fengclchn@outlook.com
>
> Date: 02/20/2023

[TOC]

![image-20230220211019523](https://histone-obs.obs.cn-southwest-2.myhuaweicloud.com/noteImg/image-20230220211019523.png)

## 第一次提交

```c++
#include <iostream>
#include <string>
#include <vector>
#include <sstream>
#include <algorithm>
using namespace std;

int main()
{
    string in;
    while (getline(cin, in))
    {
        stringstream ss(in);
        string t;
        vector<string> arr;
        while (getline(ss, t, ','))
        {
            arr.push_back(t);
        }
        sort(arr.begin(), arr.end());
        for (int i = 0; i < arr.size(); ++i)
        {
            cout << arr[i];
            if (i != arr.size() - 1)
            {
                cout << ",";
            }
        }
        cout << endl;
    }
    return 0;
}
```

