---
title: "I am so glad I largely skipped over the C++ generation of coding"
date: "2014-05-12"
tags: 
  - "c"
  - "opencv"
---

As I get back into coding, I've had to jump into some C++ code to do some OpenCV bindings for Node. And wow am I reminded of how glad I am to have basically skipped C++ as a tool. I grew up on C and ASM which always felt natural, an obvious mapping to the machine. Now I use Node and Python, with simple object support and nice type behaviour. C++ just seems like an utter backwater. I don't even begin to understand what all this really does:

```
Local<Object> mean = Matrix::constructor->GetFunction()->NewInstance();
```

Anyway if you are messing with OpenCV, it throws some horribly obtuse error messages:

```
OpenCV Error: Assertion failed (scn == 3 && (dcn == 3 || dcn == 4) && (depth == CV_8U || depth == CV_32F)) in cvtColor, file /opt/local/var/macports/build/_opt_mports_dports_graphics_opencv/opencv/work/opencv-2.4.9/modules/imgproc/src/color.cpp, line 4040
libc++abi.dylib: terminating with uncaught exception of type cv::Exception: /opt/local/var/macports/build/_opt_mports_dports_graphics_opencv/opencv/work/opencv-2.4.9/modules/imgproc/src/color.cpp:4040: error: (-215) scn == 3 && (dcn == 3 || dcn == 4) && (depth == CV_8U || depth == CV_32F) in function cvtColor
```

No idea what all that really means, but I've found it is almost always the case that I have a type mismatch. The documentation slings around matrices like they are all the same, but obviously it is important to pay attention to the differences between color images, grayscale, and binarized images, and be very intentional about their use.
