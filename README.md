# Go Array Index Out of Bounds
This example demonstrates a common error in Go: accessing an array element beyond its defined index.  Go arrays are zero-indexed, meaning the first element is at index 0, and the last element is at index len(a)-1, where len(a) is the length of the array.

Attempting to access an element outside this range will result in a runtime panic.  This is a common source of bugs, especially when dealing with loops and array manipulation.

**The bug:** The loop in `bug.go` iterates from 0 to 10 (inclusive), but the array `a` only has a length of 10 (indices 0 to 9).  The attempt to access `a[10]` causes the panic.

**The solution:** `bugSolution.go` corrects this by changing the loop condition to `i < 10`, ensuring that the loop only iterates within the valid index range of the array.