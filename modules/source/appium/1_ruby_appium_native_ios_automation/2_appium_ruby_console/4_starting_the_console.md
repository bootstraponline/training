To start the Appium Ruby Console for use with iOS, the app path is required.

In this case we're developing locally, so let's create an appium.txt with that path.

> $ nano appium.txt
> DEVICE="ios"
> APP_PATH="./UICatalog.app"


The appium.txt contains two important pieces of information.

DEVICE is the type of device we're automating.
In this case, the target operating system is ios.

APP_PATH is the path to UICatalog.app.
The ruby console is able to parse relative paths. This path will then be converted to an absolute path which appium
uses to identify which app to install on the simulator.

- TODO: Ruby code for the test.