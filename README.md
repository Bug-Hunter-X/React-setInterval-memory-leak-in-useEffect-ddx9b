# React setInterval Memory Leak
This example demonstrates a common mistake in React: using setInterval within useEffect without proper cleanup. This leads to memory leaks and unexpected behavior.

**Problem:**
The setInterval function inside useEffect continues to run even after the component unmounts. This is because the return function, responsible for clearing the interval, is missing.

**Solution:**
The solution involves returning a cleanup function from useEffect to clear the interval when the component unmounts.