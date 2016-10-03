# logback-android-utils
A small library that conveniently provides additional features for logback-android:

- Setting the root level at runtime
- Set the threshold filter of an appender. This allows for example to change the level of the logcat or a file appender
- Getting all log files
- Find the newest log file

The central logback-android logic is encapsulated in [Logs](src/main/java/info/schnatterer/logbackandroidutils/Logs.java)
 
For an example see [logback-android-demo](https://github.com/schnatterer/logback-android-demo/).

You can use it via JitPack:
Add the following maven repository to your build.gradle

	allprojects {
		repositories {
			...
			maven { url "https://jitpack.io" }
		}
	}
Then add the actual dependency

	dependencies {
	        compile 'com.github.schnatterer:logback-android-utils:1.0.0'
	}
    
