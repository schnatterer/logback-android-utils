logback-android-utils
====================

 [![Build Status](https://jenkins.schnatterer.info/job/logback-android-utils/badge/icon)](https://jenkins.schnatterer.info/job/logback-android-utils/)
 [![](https://jitpack.io/v/schnatterer/logback-android-utils.svg)](https://jitpack.io/#schnatterer/logback-android-utils)
 [<img alt="powered by openshift" align="right" src="https://www.openshift.com/images/logos/powered_by_openshift.png"/>](https://www.openshift.com/)
 
A small library that conveniently provides additional features for logback-android:

- Setting the root level at runtime
- Set the threshold filter of an appender. This allows for example to change the level of the logcat or a file appender
- Getting all log files
- Find the newest log file

The central logback-android logic is encapsulated in [Logs](src/main/java/info/schnatterer/logbackandroidutils/Logs.java)
 
For an example see [logback-android-demo](https://github.com/schnatterer/logback-android-demo/).
For a real-life example see [nusic](https://github.com/schnatterer/nusic).

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
    

# Jenkins
Running [Jenkinsfile](Jenkinsfile) with the [pipeline plugin](https://wiki.jenkins-ci.org/display/JENKINS/Pipeline+Plugin) (tested with version 2.4) requires
- A JDK defined as  Jenkins tool (see [Jenkinsfile](Jenkinsfile) for name of JDK tool)
- Maven defined as Jenkins tool (see [Jenkinsfile](Jenkinsfile) for name of Maven tool)
- Optional: You can add a build parameter `RECIPIENTS` that contains a comma-separated list of all email recipients
