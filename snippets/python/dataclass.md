---
title: dataclass
---
from dataclasses import dataclass

@dataclass
class InventoryItem:
    name: str
    unit_price: float
    quantity_on_hand: int = 0
    mylist: list[int] = field(default_factory=list)
