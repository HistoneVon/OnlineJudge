# 040_JDCodeTop02 反转链表

> Author: fengclchn@outlook.com
>
> Date: 02/21/2023

[TOC]

* LeetCode0206：012
* ACM模式

## 第一次提交

```c++
#include <iostream>
#include <vector>
using namespace std;

struct ListNode
{
    int val;
    ListNode *next;
    ListNode() : val(0), next(nullptr) {}
    ListNode(int n) : val(n), next(nullptr) {}
    ListNode(int n, ListNode *next) : val(n), next(next) {}
};

ListNode *create(vector<int> &nums)
{
    ListNode *head = new ListNode(0);
    ListNode *p;
    ListNode *pre = head;
    for (int i = 0; i < nums.size(); i++)
    {
        p = new ListNode(nums[i]);
        pre->next = p;
        pre = pre->next;
    }
    return head->next;
}

bool fresh(ListNode *head)
{
    try
    {
        ListNode *dummyHead = new ListNode(-1);
        dummyHead->next = head;
        ListNode *curr;
        while (dummyHead->next != nullptr)
        {
            curr = dummyHead->next;
            dummyHead->next = dummyHead->next->next;
            delete curr;
        }
        delete dummyHead;
        return true;
    }
    catch (const std::exception &e)
    {
        std::cerr << e.what() << '\n';
        return false;
    }
}

ListNode *reverseList(ListNode *head)
{
    if (head == nullptr)
    {
        return nullptr;
    }
    ListNode *prev = nullptr;
    ListNode *curr = head;
    ListNode *next = head->next;
    while (next != nullptr)
    {
        if (curr == head)
        {
            curr->next = nullptr;
        }
        prev = curr;
        curr = next;
        next = next->next;
        curr->next = prev;
    }
    return curr;
}

int main()
{
    int n;
    vector<int> nums;
    while (cin >> n)
    {
        nums.push_back(n);
        if (cin.get() == '\n')
        {
            ListNode *l = create(nums);
            l = reverseList(l);
            ListNode *p = l;
            while (p != nullptr)
            {
                cout << p->val << " ";
                p = p->next;
            }
            cout << endl;
            vector<int>().swap(nums);
            fresh(l);
        }
    }
    return 0;
}
```

* 我的（自己又盲写了一遍）

```c++
ListNode* reverseList(ListNode* head) {
  if (head == nullptr) {
    return nullptr;
  }
  ListNode* prev = nullptr;
  ListNode* curr = head;
  ListNode* next = head->next;
  while (next != nullptr) {
    if (curr == head) {
      curr->next = nullptr;
    }
    prev = curr;
    curr = next;
    next = next->next;
    curr->next = prev;
  }
  return curr;
}
```

* 代码随想录的

```c++
class Solution {
public:
    ListNode* reverseList(ListNode* head) {
        ListNode* temp; // 保存cur的下一个节点
        ListNode* cur = head;
        ListNode* pre = NULL;
        while(cur) {
            temp = cur->next;  // 保存一下 cur的下一个节点，因为接下来要改变cur->next
            cur->next = pre; // 翻转操作
            // 更新pre 和 cur指针
            pre = cur;
            cur = temp;
        }
        return pre;
    }
};
```

