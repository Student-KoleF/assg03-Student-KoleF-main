---
name: 'Task 2: Implement `findCandidateProcess`  member function'
about: Task 2 for Students
title: 'Task 2: Implement `findCandidateProcess` member function'
labels: enhancement
assignees: ''

---

**Description**

Implement the missing `findCandidateProcess()` member function.  This
function again takes an array of currently available resources.  This
function will return a process identifier.  It also takes an array of
boolean flags that indicate whether each process is currently done or
is not yet finished in this simulation.  This id is the first
candidate process that is found whose need can be met.  If no current
process is a candidate whose needs can be met, then this function
returns the defined constant `NO_CANDIDATE`.

**Suggested Solution**

You need to check all processes, using the `needsAreMet()` function, starting from process 0 to
the last process currently in the simulation.  If the process is not yet done, and if its
needs can be met, then return the process id of the candidate process that was
found.  If all processes are checked, and none are candidates, return the
`NO_CANDIDATE` defined constant instead.

The pseudocode for the `findCandidateProcess()` function thus would
look something like this:

```
for each process:
   if process not yet completed and processes needs are met
      return the process id

otherwise if no process was found, return NO_CANDIDATE
```

**Additional Requirements**

- You are required to reuse the previous tasks `needsAreMet()` in the implementation
  of this funciton to test each process and see if a candidate process exists
  given the current available resources.
- You are required to use the global defined `NO_CANDIDATE` constant in this function,
  do not return a magic number or define some other return value.
- You are required to provide properly formatted Doxygen documentation for this
  function in your implementation file.

