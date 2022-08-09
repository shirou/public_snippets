---
title: from json
desc: aka unmarshal
tags:
  - golang
---
var p Foo
if err := json.Unmarshal(b, &p); err != nil {
	fmt.Println(err)
}
