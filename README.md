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
```
	
### Step 3

Inisialize the webview in your activity where you have the webview.

```java
new AdBlockerWebView.init(this).initializeWebView(webView);
```

### Step 4

Now to block ads we need to add this code in the WebViewClient so extentd the WebViewClient for your webview like this and then in the class overide this method.


```java
webView.setWebViewClient(new Browser_home());
```

```java
private class Browser_home extends WebViewClient {

        Browser_home() {}

        @SuppressWarnings("deprecation")
        @Override
        public WebResourceResponse shouldInterceptRequest(WebView view, String url) {

            return AdBlockerWebView.blockAds(view,url) ? AdBlocker.createEmptyResource() :
                    super.shouldInterceptRequest(view, url);

        }

    }
```
