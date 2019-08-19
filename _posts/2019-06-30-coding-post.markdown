---
layout: post
title: 테스트
subtitle: Coding Post
description: 백준 15969번 C++
date:   2019-05-23 21:03:36 +0530
edit:   2019-05-23 21:03:36 +0530
categories: C++
---

```cpp
#include <iostream>
using namespace std;

int main() {
    int a;
    cin >> a;
    int b[a+1];
    
    for(int i=0; i<a; i++) cin >> b[i];
    
    b[a]=b[0]; b[a+1]=b[0];
    
    for(int i=1; i<a; i++)
    {
        if(b[i] != b[a] && b[i] != b[a+1]) {
            if(b[i] > b[a+1]) {
                b[a+1] = b[i];
            } else if(b[i] < b[a]) {
                b[a] = b[i];
            }
        }
    }
    
    cout << b[a+1]-b[a];
}
```

C++ 코드블럭