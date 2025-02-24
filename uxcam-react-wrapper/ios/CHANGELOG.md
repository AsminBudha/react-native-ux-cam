# UXCam iOS framework


## Release Notes ##

Version   | Changes
---------- | ----------
3.1.5	| Additional symbols from 3rd party libraries changed. 
3.1.4	| Added API to create a list of screen names to not add to the timeline in automatic screen tagging mode
3.1.3	| Added marker of keyboard location to the schematic recording
		| Added an 'ultra low' video quality setting
3.1.2 	| Fix to mobile data upload limits
		| Fix for symbol conflict in internal copy of 3rd party library
3.1.1	| Internal changes for performance and stability 
3.1.0	| Change screen capture to schematic capture process
		| Opt In changes to split out screen recording as specific option - **screen recording off by default** 
		| Fix session video when starting up with occluded screen
		| Add reasons why screen video hasn't been recorded
		|  
		|
3.0.6	| Add `occludeSensitiveViewWithoutGesture` and `occludeSensitiveScreen:hideGestures:` API methods
		| Adjust work queues for event capture 
		| Add nullable decoration to session and user url methods
		| Adjust some internal timers to handle external time changes
		| Fix an orientation regression with sessions that start in landscape orientation
3.0.5	| Stop recording gestures when screen recording is paused or full screen is occluded
		| Fix an issue on initial setup of data capture
3.0.4	| Improvements to filter handling when account is low on sessions left to record
3.0.3	| Fix a session management issue
3.0.2 	| Work around the iOS bug that causes excessive screen capture time on wide colour devices
3.0.1	| Fixing some header file deprecations to avoid ambiguous method errors in Swift
		| Improved handling of devices with low levels of available storage
3.0.0  	| Extensive refactoring of the internals of the SDK to support new features
		| Added session filters for screen name, session duration, number of interactions
		| Added support for offline session recording
		| Added support for data-only sessions (screens visited, number of interactions, event timeline etc. without a screen video)
		| Re-factored the UXCam API on iOS and Android to be more similar and iOS to better conform with standard naming practices
		| Re-factored the event recording system to include user and session events as well as general timeline events
		| Note: Sep 2018: Several v3 features require using the new dashboard that is coming soon - talk to support to get preview access 
		|
2.5.18	| Adding `unOccludeSensitiveView` method
		| Fixing a problem that exposed sensitives views for their first frame on screen in some circumstances
2.5.17	| Fixing a problem with tag collection from multiple threads
		| Fixing memory leaks when recording screens with video content
2.5.16	| Fixing a 2.5.15 introduced bug with network reachability
2.5.15	| Fixing some more iOS11 warnings about documentation in UXCam.h
		| Problems when recording iPad apps in split mode have been fixed
		| [BETA] `allowShortBreakForAnotherApp` method - will pause the recording while the user goes out to another.
		| [BETA] `StopRecordingScrollingOnStutterOS` method to work around iOS11.2 problems
2.5.14	| Fixing a warning in iOS11
2.5.13	| Adjusting the occlusion of sensitive views during animations
2.5.12	| Adjusting the occlusion of secure and/or UITextFields to be less sensitive to screen construction order
2.5.11	| Removed the default setting of `tagUsersName` from UIDevice.currentDevice.name - there is no default now
2.5.10	| Fixing a problem with screen names not being registered if no events occured on that screen
2.5.9	| Adding `occludeAllTextFields` method
		| Adding `SetMultiSessionRecord` and `GetMultiSessionRecord` methods
		| Adding `PauseScreenRecording` and `ResumeScreenRecording` methods
		| Adding `cancelCurrentSession` method
		| Restoring the `DisableCrashHandling` method
		| Adding method to access sessions awaiting upload. See `PendingUploads` for information
		| Adding method to upload any pending sessions. See `UploadingPendingSessions` for details
		| Improved occlusion of sensitive views in a moving scrollview
2.5.8	| Trapping nil value for screen name that would cause a crash 
		| Adding `SetAutomaticScreenNameTagging` to disable automatic screen name capture
2.5.7	| Capturing app version as well as build number for dashboard
2.5.6	| Fixing a problem with capturing Swift crashes
		| Fixing a problem with `NSCameraUsageDescription` when submitting apps from XCode8
		| Adding support for more quality settings
		| Optimising some code paths
2.5.5	| Fixing a bug that caused video problems on iOS8
2.5.4	| Improvements in gesture timeline
		| Improved capture of screen name at app start
		| Better handling of sensitive views after app comes out of background
		| Improved capture of crashed sessions
2.5.3	| Don't occlude sensitive views that are hidden
		| Fixing the `SessionURL` path
2.5.2	| Fixing a 3G/wifi upload issue
2.5.1	| Improving upload code
2.5.0	| Refactoring of sending multiple sessions in one upload
2.4.2	| Fixing user session URL
2.4.1	| Change in how user country is captured
2.4.0	| First version working as a Swift module
		| Requires XCode7
		| iOS7 is no longer tested against/supported, but should continue working
2.3.4	| Changing timer resets
2.3.3	| Adding verbose internal logging to SDK
2.3.1	| Internal improvements
2.3.0	| Ability to record just one session per run
2.2.2	| Trapping some crash handler errors
2.2.1	| Fixing log capture when more than one session in a run
2.2.0	| Adding log output capture and upload
2.1.1	| Fixing documenation links
2.1.0	| Adding app variant support to `startUXCam` methods
		| Exposing the occulde screen method to Cordova
		| Fixing session and user URLs
2.0.3	| Handle the case of an app having no icon file
2.0.2	| Fixing some version number values in the uploaded data
2.0.1	| Removed unused data fields from uploaded data
2.0.0	| Major re-engineering of the SDK in terms of backend used
