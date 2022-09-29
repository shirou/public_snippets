---
description: generate array of int
tags:
  - golang
---
func enumerate(min, max int) []int {
    a := make([]int, max-min+1)
    for i := range a {
        a[i] = min + i
    }
    return a
}
