# 042_剑指Offer58-II 左旋转字符串

> Author: fengclchn@outlook.com
>
> Date: 02/22/2023

[TOC]

## 第一次提交

```c++
#include<string>
#include<algorithm>
using namespace std;

class Solution {
public:
    void reverseStr(string& s, int start, int end) {
        for (int i = start, j = end; i < j; ++i, --j) {
            swap(s[i], s[j]);
        }
    }
    string reverseLeftWords(string s, int n) {
        reverseStr(s, 0, n - 1);
        reverseStr(s, n, s.size() - 1);
        reverseStr(s, 0, s.size() - 1);
        return s;
    }
};
```

![image-20230222162234682](https://histone-obs.obs.cn-southwest-2.myhuaweicloud.com/noteImg/image-20230222162234682.png)

## 代码随想录

* [代码随想录 (programmercarl.com)](https://www.programmercarl.com/剑指Offer58-II.左旋转字符串.html)