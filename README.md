LFLogfly
========

[iOS] A logger with batch data transferring to backend.

![](https://dl.dropboxusercontent.com/u/7817937/_github/logfly.png)

STATUS
---

![](http://progressed.io/bar/0)

Usage
---

```objc
+ (FLLogfly *)sharedLogger;

- (void)log:(NSString *)aString;

- (void)pageView:(UIViewController *)viewController;
- (void)event:(NSString *)tag forViewController:(UIViewController *)viewController;
```

```objc
[[FLLogfly sharedLogger] log:@"event.NewUserViewController.button.create_user.push"];
// or
[[FLLogfly sharedLogger] event:@"button.create_user.push" forViewController:self];
```

Will store the log data in SQLite and send them in background thread at appropriate span.

And `LFLogfly` concerns duplication and network failures!

LICENSE
---

The MIT License (MIT)

Copyright (c) 2014 kaiinui

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
