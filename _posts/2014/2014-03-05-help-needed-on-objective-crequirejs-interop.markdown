---
title: "Help needed on objective-c/requirejs interop"
date: "2014-03-05"
---

I am hosting the webview controller in an OSX app. I have followed the code sample in [calljs](https://developer.apple.com/library/mac/samplecode/CallJS/Introduction/Intro.html#//apple_ref/doc/uid/DTS10004241) and i can successfully call javascript functions inside script tags from objective-c. This integration requires that the objective-c program know the name of the javascript function. for instance i have a javascript function called "objective\_c\_entry()", and in my objective c wrapper, i can call that entry point using:

```
NSString *callResult = [[webView windowScriptObject] callWebScriptMethod:@"objective_c_entry" withArguments:args];
```

Now I want to move all my javascript into require.js modules; i am not clear how to reference a function in a require.js module from within objective-c. if i am moving my "objective\_c\_entry" function into a require.js module named "integration", what string do I pass to callWebScriptMethod?
