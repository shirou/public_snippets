---
description: remove 0, False, empty values from a list
---
def compact(lst):
    return list(filter(None, lst))


compact([0, 1, False, 2, '', 3, 'a', 'b'])  # [ 1, 2, 3, 'a', 'b']
