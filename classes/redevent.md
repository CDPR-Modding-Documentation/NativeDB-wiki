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

# redEvent

## Description

Dispatched throughout game session to trigger gameplay logic, for various purposes:

* combat
* traffic
* ...

Event can be dispatched in-game on instances of class inheriting from \[Entity].

More info and code snippets [there](https://cyb3rpsych0s1s.github.io/4ddicted/patterns/events.html#event-inherited-from-red-event).

If you're looking to dispatch events outside of game sessions, see [wiki of Codeware](https://github.com/psiberx/cp2077-codeware/wiki#custom-events) for custom events.
