+++
title = 'Go的使用记录'
date = 2024-09-22T11:47:03+08:00

categories = ["Go"] 
tags = ["go语法","记录"]

+++



# 在 Go 语言中，`cnt := [2]int{}` 

- `cnt` 是一个变量，使用短变量声明 (`:=`) 定义。
- `[2]int` 表示这是一个长度为 `2` 的 **数组**，数组的元素类型是 `int`。
- `{}` 表示这个数组被初始化为零值，也就是所有的元素都被初始化为整型的零值 `0`。

### 示例代码
```go
package main

import "fmt"

func main() {
    cnt := [2]int{}
    fmt.Println(cnt) // 输出: [0 0]
}
```

### 细节
- 数组是固定长度的，`[2]int` 表示它的长度为 `2`，如果需要动态长度的集合，可以使用切片 (`[]int`)。
- 如果你想明确初始化数组的值，可以写成这样：
  ```go
  cnt := [2]int{1, 2}
  fmt.Println(cnt) // 输出: [1 2]
  ```

- 如果只部分初始化，未赋值的部分会使用零值：
  ```go
  cnt := [2]int{1}
  fmt.Println(cnt) // 输出: [1 0]
  ```



# range循环时需要注意点



错误的代码：

```go
banSet := make(map[string]struct{})
for word := range bannedWords {
    banSet[word] = struct{}{}
}
```

是不正确的，因为 `range` 关键字在 Go 语言中用于遍历集合（如数组、切片、映射、字符串等）时，会同时返回**索引**和**值**。

在你的写法中，`for word := range bannedWords` 只返回了 `bannedWords` 的索引（即数组或切片的索引），而不是你实际想要的单词。

正确的写法应该是：

```go
banSet := make(map[string]struct{})
for _, word := range bannedWords {
    banSet[word] = struct{}{}
}
```

## 解释：
1. **`for _, word := range bannedWords`**：
   - `range bannedWords` 会返回两个值：第一个是索引，第二个是 `bannedWords` 中的每个元素（即单词）。
   - 你用 `_` 来忽略索引，因为你只关心单词 `word`。

## 为什么不能直接使用 `for word := range bannedWords`？
- `range bannedWords` 实际上返回的是索引和值，`for word := range bannedWords` 只取了第一个值，也就是索引，而不是你期望的单词。
- 你需要第二个值（单词）来填充 `banSet`，因此你必须使用 `for _, word := range bannedWords`。

## 总结：
你需要在遍历 `bannedWords` 时获取每个单词的值，因此必须用 `for _, word := range bannedWords`。
