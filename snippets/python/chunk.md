---
title: chunk a list
description: chunk a list to smaller lists with specified size
---
def chunk(list, size):
    return [list[i:i+size] for i in range(0,len(list), size)]
