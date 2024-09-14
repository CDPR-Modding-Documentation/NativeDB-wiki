---
layout:
  title:
    visible: true
  description:
    visible: false
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
---

# gameTransactionSystem

## Functions

#### GiveMoney(target: handle:gameObject, amount: Int32, currency: CName) -> Bool

Known currency values: `n"money"`.

#### RemoveMoney(obj: handle:gameObject, amount: Int32, currency: CName) -> Bool

Known currency values: `n"money"`.

#### TransferMoney(source: handle:gameObject, target: handle:gameObject, amount: Int32, currency: CName) -> Bool

Known currency values: `n"money"`.
