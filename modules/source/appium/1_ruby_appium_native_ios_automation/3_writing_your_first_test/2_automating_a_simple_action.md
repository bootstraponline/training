Taking what we've learned from the previous module, it's time to write a complete test.

You'll notice that the commands are exactly the same as what we used in the console.
Literally, code can be copied and pasted to and from the console to form production tests.

One common source of errors is related to timing. Specifically in the console,
the implicit wait is turned to zero for immediate feedback. That means when an element isn't found
the test ends immediately because an element not found exception is raised.

To overcome these timing problems, the wait helper method is useful.

- TODO: Ruby code for the test.