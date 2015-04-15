Researching computer vision topics, I often need to grab images/video from webcams and video acquisition hardware, and most of times I use OpenCV default camera framework. However, for recent projects I had to handle camera's properties more in depth (especially to handle fps), and OpenCV resulted bugged and inappropriate. I've spent a day searching the net for an easy interface (eg, which allows you to write a camera-preview app less than 20 lines of code long), with basic functions to handle settings, but I couldn't find any.
At last I've downloaded a sample v4l2 demo app (700-800 lines of code, but I had already worked with v4l before) and built a wrapper class around it, building the library I had looked for. Now I'm releasing it, for all those coders who need it and don't have time to learn the v4l2 low level API.
The library provides raw YUYV output as well as BGR24 OpenCV's IplImage objects.

The SVN currently features 2 applications:
-libv4l2cam : the camera grabber software
-libv4l2stereo : a feature-based stereo matching system (making use of libv4l2cam and OpenCV libraries)
