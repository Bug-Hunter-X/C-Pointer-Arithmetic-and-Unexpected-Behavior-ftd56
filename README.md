# C Pointer Arithmetic and Unexpected Behavior

This repository demonstrates a common error in C programming related to pointer arithmetic. The primary issue is the risk of accessing memory outside the allocated space, leading to unpredictable consequences.

**The Problem:**
The provided `bug.c` code snippet modifies a variable via a pointer, which is a common operation, but it doesn't contain inherent errors in the direct use of pointers.  However, the subtle error lies in the potential for this to become a larger problem if the pointer arithmetic is extended to point outside of the intended memory locations (e.g., when the pointer is incremented or decremented to point outside of the allocated array/object).  This can lead to segmentation faults, unexpected data corruption or program crashes.