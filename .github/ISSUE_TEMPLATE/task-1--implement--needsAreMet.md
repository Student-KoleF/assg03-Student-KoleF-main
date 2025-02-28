---
name: 'Task 1: Implement `needsAreMet()` member method'
about: Task 1 for Students
title: 'Task 1: Implement `needsAreMet()` member method'
labels: enhancement, good first issue
assignees: ''

---

**Description**

Implement the `needsAreMet()` member method.  This method takes a process
identifier and an array of currently available resources as input.  It will
return a boolean result of true if the needs can be met for the indicated process
with the current available resources.  It will return false if the needs cannot
be met for the process.

**Suggested Solution**

The `State` class has a 2D array called `needs` which are the needs of all of the
processes currently in the simulation.  Each row of the `needs` matrix has the needs
for a process.  You need to check each amount of needed resource for the indicated
process againist the currently available resources given to this function.  If the
need is greater than the currently available, you should return `false` immediately.
But if you check all of the resources needs, and they all end up being less than or
equal to the available resources, then you should return true.


**Additional Requirements**

- You are required to provide properly formatted Doxygen documentation for this
  function in your implementation file.
