---
title: insert into middle
tags:
  - golang
---
// insert inserts c into a on index
func insert(a []int, c int, index int) []int {
    return append(a[:index], append([]int{c}, a[index:]...)...)
}
