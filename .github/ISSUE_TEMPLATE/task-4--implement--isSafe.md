---
name: 'Task 4: Implement `isSafe()` member method'
about: Task 4 for Students
title: 'Task 4: Implement `isSafe()` member method'
labels: enhancement
assignees: ''

---

**Description**

Implement the `isSafe()` member method.  This is the main method that determins if
the current "state" of the system is considered safe or unsafe.

You will be reusing (directory and/or indirectly) all 3 of the previous task methods
to implement the `isSafe()` method.  `isSafe()` return a boolean result of `true`
if the state is safe, and `false` if it is not.  No parameters are given as input
to the `isSafe()` method, it uses the state of the class in the member variables
to do its work and determine its answer.

**Suggested Solution**

The pseudo-code of the steps you need to perform are as follows:

```
1. Make a copy of the State resourceAvailable vector using the copyVector() function.
   This will be the currentAvailable vector, which is initially equal to the
   available resources, but if/when processes complete we release resources back to the
   system and keep track of the currently available resources in this vector.

2. Create a list of all processes called completed. Represent the list as an array of bool flags.
   The completed array keeps track of which processes have been selected and run to completion.
   Thus initially all processes should be marked as false, as all processes start out as
   not completed initially.

3. Search for a candidate process from the uncompleted processes.  This will be a loop
   that should keep being performed until no candidate process is found that can be selected
   to run to completion.  You should use the findCandidateProcess() function to search for
   the next potential candidate process to run.

	3.1 If we found a candidate process, release its allocated resources back to the available
	    resources using releaseAllocatedResources().  Also mark the candidate process as
		completed.

	3.2 If no candidate was found, terminate the search loop

4. As a final test, after the search completes, if all processes were marked as
   complete, then the state is safe, so return true.  Otherwise if 1 or more
   processes did not complete, then the state is unsafe and you return false.
```

**Additional Requirements**

- You are required to directly reuse `findCandidateProcess()` and
  `releaseAllocatedResources()` in your solution.  Since `findCandidateProcess()`
  reuses `needsAreMet()`, you directly or indirectly reuse all 3 of the preliminary
  methods in the implementation of `isSafe()`.
- You are required to provide properly formatted Doxygen documentation for this
  function in your implementation file.
