<h1> Android WebView example</h1>

<h3>AndroidManifest.xml</h3>

```xml
<uses-permission android:name="android.permission.INTERNET"/>
```

<h3>layout.xml</h3>

```xml
<WebView
  android:layout_width="match_parent"
  android:layout_height="400dp"
  android:id="@+id/webView"
  android:layout_alignParentLeft="true"
  android:layout_alignParentStart="true"
  android:layout_alignParentTop="true" />
```

<h3>Main.java</h3>

```java
WebView webView = (WebView) this.findViewById(R.id.webView);
editText = (EditText) this.findViewById(R.id.editText);

webView.getSettings().setJavaScriptEnabled(true);
webView.loadUrl("https://github.com/pethoalpar");

webView.setWebViewClient(new WebViewClient(){
    @Override
    public boolean shouldOverrideUrlLoading(WebView view, WebResourceRequest request) {
        return false;
    }
});
```
