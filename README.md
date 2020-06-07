# WebViewAdblock

Instalation guide 

#1 Add it in your root build.gradle at the end of repositories:
 
```gradle
	allprojects {
		repositories {
			...
			maven { url 'https://jitpack.io' }
		}
	}
 ```
 
 Step 2. Add the dependency
 
 ```gradle
 	dependencies {
	        implementation 'com.github.MonsterTechnoGits:WebViewAdblock:Tag'
	}
 
