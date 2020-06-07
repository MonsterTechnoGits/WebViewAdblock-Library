# WebViewAdblock

Android webview Adblocker is a simple library to block ads in webview. this code is basicaly stop the ads and remove the html from it and render it again. 

## How do I use it?
### Step 1

#1 Add it in your root build.gradle at the end of repositories:
 
```gradle
	allprojects {
		repositories {
			...
			maven { url 'https://jitpack.io' }
		}
	}
 ```
 
 ### Step 2
 
 Add the dependency in app level build.gradle file
 
 ```gradle
 	dependencies {
	        implementation 'com.github.MonsterTechnoGits:WebViewAdblock:Tag'
	}
 
