---
title: read from stdin
tags:
  - golang
---
import (
        "bufio"
        "fmt"
        "os"
)

func main() {
        s := bufio.NewScanner(os.Stdin)
        for {
                if ok := s.Scan(); !ok {
                        break
                }
                line := s.Text()
                fmt.Println(line)
        }

}
