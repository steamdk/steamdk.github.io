+++
title = 'CppVsCode代码快捷模板'
date = 2024-11-15T16:09:30+08:00



categories = ["cpp"]
tags = ["模板" , "cpp"]

+++



# Cpp各类模板设置

## 插入代码模板

```json
"nameXXX": {
		"prefix": "XXX操作码",
		"body": [
			"xxxxxx",
			"xxxxxx",
			"yyyyyy",
			"yyyyyy",
			"$0"
		]
	},

```



## 头文件 

```cpp
#pragma GCC optimize("O2")

#include<bits/stdc++.h>
#include <iostream>      // cin/cout
#include <cstdio>        // printf/scanf
#include <algorithm>
#include <vector>        // 容器
#include <string>        // 字符串
#include <stack>         // 栈
#include <queue>         // 队列
#include <unordered_map> // 哈希表
#include <unordered_set> // 哈希表 set
#include <memory>        // 智能指针
#include <functional>
#include <numeric>
#include <ranges>
#include <cstring> 
#include <bitset>
#include <cmath>

using namespace std;

typedef long long ll;       // long long为ll
typedef long double ld;     // long doubleld
typedef pair<int, int> pii; // pair<int, int>pii
typedef pair<ll, ll> pll;   // pair<ll, ll>pll
typedef vector<int> vi;     // vector<int>vi

const long long inf = numeric_limits<long long>::max(); // 无穷大
const int N = 100100; // 100 百 , 100100 十万 , 1100100 一百万 , 100100100 一亿

void Mysolve(){
    
    
}

int main(){
    ios::sync_with_stdio(false);
    cin.tie(NULL);
    cout.tie(NULL);
    //---------优化

    Mysolve();
    return 0;
}
```



> cpp.json 设置

```json
{
	"HEADER": {
		"prefix": "H",
		"body": [
			"#pragma GCC optimize(\"O2\")",
			"",
			"#include<bits/stdc++.h>",
			"#include <iostream>      // cin/cout",
			"#include <cstdio>        // printf/scanf",
			"#include <algorithm>",
			"#include <vector>        // 容器",
			"#include <string>        // 字符串",
			"#include <stack>         // 栈",
			"#include <queue>         // 队列",
			"#include <unordered_map> // 哈希表",
			"#include <unordered_set> // 哈希表 set",
			"#include <memory>        // 智能指针",
			"#include <functional>",
			"#include <numeric>",
			"#include <ranges>",
			"#include <cstring> ",
			"#include <bitset>",
			"#include <cmath>",
			"",
			"using namespace std;",
			"",
			"typedef long long ll;       // long long为ll",
			"typedef long double ld;     // long doubleld",
			"typedef pair<int, int> pii; // pair<int, int>pii",
			"typedef pair<ll, ll> pll;   // pair<ll, ll>pll",
			"typedef vector<int> vi;     // vector<int>vi",
			"",
			"const long long inf = numeric_limits<long long>::max(); // 无穷大",
			"const int N = 100100; //  100100 十万 , 1100100 一百万 , 100100100 一亿",
			"",
			"void Mysolve(){",
			"    ",
			"}",
			"",
			"int main(){",
			"    ios::sync_with_stdio(false);",
			"    cin.tie(NULL);",
			"    cout.tie(NULL);",
			"    //---------优化",
			"",
			"    Mysolve();",
			"    return 0;",
			"}",
			"$0"
		]
	},

}
```



## leetcode模板

```json
	"leetcode": {
		"prefix": "lc",
		"body": [
			"#pragma GCC optimize(\"O2\")",
			"",
			"#include<bits/stdc++.h>",
			"using namespace std;",
			"",
			"const long long inf = numeric_limits<long long>::max();",
			"",
			"$0"
		]
	},
```





> 算法模板

## 高精度算法

```json



```

##



##

##

##

##

##

##

##

##

##

##

##

##

##

##

##

##

##

##

##
