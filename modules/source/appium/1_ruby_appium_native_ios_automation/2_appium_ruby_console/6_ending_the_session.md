Once we're done with a testing session, it's very important to cleanly quit.
If a session is not exited properly then appium will consider the session to still
be in progress. This blocks all future sessions from working.

In the console, the best way to quit the session is by using the "x" command.
The "x" command first ends the webdriver session, and then ends the console.

If you desire to end only the webdriver session and remain in the console,
use driver_quit.