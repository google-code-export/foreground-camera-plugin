Foreground Camera Plugin for Phonegap.

Originally by: 	- Bruno Carreira
				- Lucas Farias
				- Rafael Luna
				- Vinicius Fonseca

The default Phonegap Camera Plugin calls the native camera and this makes Android Garbage Collector to kill background applications. This plugin avoid your application to go background and be killed by Garbage Collector with other applications. We used the Phonegap source code and modified it to avoid this problem. This plugin works only with File URI. 

Adding the plugin to your project

    1) To install the plugin, move the file camera.js to your project's www folder and include a reference to it in your html files.
    2) Put the Java files in your src/ folder.
    3) Change the default Camera Plugin into res/xml/plugins.xml file to <plugin name="Camera" value="<path to your ForegroundCameraLauncher.java>"/>.
	4) Put the strings.xml in your res/values folder.
	5) Put the foregroundcameraplugin.xml in your res/layout folder.
	6) In you AndroidManifest.xml, put this permissions:
		    <uses-feature android:name="android.hardware.camera" />
			<uses-feature android:name="android.hardware.camera.autofocus" />
		And declare the Camera Activity:
			<activity
				android:name=".CameraActivity"
				android:label="ForegroundCameraPlugin"
				android:screenOrientation="landscape" >
			</activity>

Using the plugin

	See the index.xhtml.

The MIT License

Copyright (c) 2012 

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.