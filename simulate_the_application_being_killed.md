# Simulate The Application Being Killed

1. Exit your app using the home button
2. In a terminal:
	
	`adb shell ps`
	
	// then find the line with the package name of your app

	// Mac/Unix: save some time by using grep:
	
	`adb shell ps | grep your.app.package`

	// The result should look like:
	
	// USER      PID   PPID  VSIZE  RSS     WCHAN    PC         NAME
	
	// u0_a198   21997 160   827940 22064 ffffffff 00000000 S your.app.package

	// Kill the app by PID
	
	`adb shell kill -9 21997`

	// the app is now killed
	
3. Now return to the app using the task switcher. You are now on a new application instance.
	