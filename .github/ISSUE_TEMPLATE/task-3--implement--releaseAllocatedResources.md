---
name: 'Task 3: Implement `releaseAllocatedResources()`  member method'
about: Task 3 for Students
title: 'Task 3: Implement `releaseAllocatedResources()` member method'
labels: enhancement
assignees: ''

---

**Description**

Implement the missing `releaseAllocatedResources()` member function.  This function takes
a process identifier and an array of currently available resources.  All of the
allocated resources for the indicated process should be "released" by adding them back in
to the available resources.

**Suggested Solution**

There is a matrix called `allocation` in the `State` class that contains a count of the
number of allocated resources for each process.  Each row of the matrix is the allocations
for a process in the simulation.  Add all of the allocations for the indicated process into
the available resources.

The pseudocode to implement the `releaseAllocatedResources()` member functions
would look somthing like the following:

```
for each resource in the system
   add the number of allocated resources for the indicated process to the current available resources
```

**Additional Requirements**

- You are required to provide properly formatted Doxygen documentation for this
  function in your implementation file.

