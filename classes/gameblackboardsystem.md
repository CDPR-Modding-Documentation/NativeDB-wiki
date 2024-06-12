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

# gameBlackboardSystem

## Description

Blackboard is a kind of shared data storage and a framework to access/notify/listen to the data in the storage. Similar to a real blackboard, \[GameObject]s put their data on the board (\[IBlackboard]). Other objects can observe, react to and update the data.

Blackboard uses a key-value pattern to store data. Keys are defined through a \[BlackboardDefinition]. You can know what keys (ids) a \[IBlackboard] is using with its corresponding \[BlackboardDefinition]. A list of known definitions can be found in \[AllBlackboardDefinitions].

See also this post on [StackExchange](https://gamedev.stackexchange.com/a/72441).

## Functions
