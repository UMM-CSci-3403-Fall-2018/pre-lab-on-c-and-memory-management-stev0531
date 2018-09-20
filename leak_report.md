# Leak report

The memory leaks occur because memory is allocated in `strip` and is never deallocated if the string isn't only spaces. How to fix this problem is to free the allocated memory in the method `is_clean` because the allocated memory is used in that method, but it doesn't need to free the memory if the string is only spaces because memory is never allocated.

