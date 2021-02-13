---
title: test
categories: [Algorithm]
comments: true
---

전화번호부
```c++
#include <string>
#include <vector>
#include <algorithm>
using namespace std;

bool solution(vector<string> phone_book) {
    sort(phone_book.begin(), phone_book.end());
    bool answer = true;
    for(int i =0;i<phone_book.size() - 1;i++){
        if(phone_book[i].length() >= phone_book[i+1].length()) continue;
        if(phone_book[i+1].substr(0,phone_book[i].length()) == phone_book[i]){
            answer = false;
            break;
        }
    }
    return answer;
}
```