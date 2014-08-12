Cordova Sample Plugin
=====================

It is not obvious from the documentation how a custom Cordova plugin should be written to integrate it with a Sencha Touch app. This small plugin proofs how this is possible. 

This sample plugin is derived work from the [Steroids Echo Plugin](https://github.com/AppGyver/steroids-echo-plugin) and [Cordova Echo plugin example](http://cordova.apache.org/docs/en/3.0.0/guide_hybrid_plugins_index.md.html#Plugin%20Development%20Guide). It has been tested using:

* Sencha Cmd v5.0.0.160
* Sencha Touch v2.3.1.410
* Cordova v3.5.0-0.2.6

* XCode v5.1.1

The plugin does *not* currently work for Android

##Usage

The plugin sends a text string back from the native layer. To use it:

1. Add the plugin to your project

   cordova plugin add https://github.com/quiaro/cordova-sample-plugin.git

2. Add the following snippet of code in a controller or an event handler in your Sencha Touch app:

```
var myPlugin = cordova.require("com.quiaro.plugin.Echo.Echo");

// Call the plugin's echo method
myPlugin.echo("Think left and think right and think low and think high. Oh, the thinks you can think up if only you try!", function(message) {
    alert("Dr.Seuss says: " + message);
});
```