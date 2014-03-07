Now that we have the code written and it's following best practices, let's investigate a new way to run it.

One way to run the test is to copy and paste the lines into the console.
This can be done line by line when debugging. You could also copy and paste the entire test.

When running a full test, it's often preferable to use the 'rake' command. It's faster
than manually opening the console and copy and pasting code.

> rake android[test_name]

The Rakefile for this project is setup to define an android task. That task accepts
the test name as an argument.

Running a single test this way is great for debugging as the individual lines of the source code
are printed to the console. It also reproduces how the test will be run in continuous integration.
If there are timing issues then they will be apparent when everything is run together.