---
title: "Weekend software experiment -- Facebook's Deepmask"
date: "2016-08-29"
---

[Facebook open-sourced](https://code.facebook.com/posts/561187904071636) its [Deepmask and Sharpmask](https://github.com/facebookresearch/deepmask) codebases last week for object segmentation in a scene. In the past I've tried traditional CV methods to do object masking, and it is kind of a disaster, you end up with a very finicky codebase full of heuristics and hacks, which fails as soon as it sees a new kind of image. Seems like an archetypical use case for neural nets. So seemed worth giving it a try.

Deepmask and Sharpmask come with pretrained models based on the [COCO dataset](http://mscoco.org/), it looks laborious to label a new dataset without benefit of some mechanical turk-like process, so I decided to stick with the pretrained models.

To avoid polluting my system, and to share with the rest of the team, I decided to bring this all up in a docker container. Because our build environment has some unique characteristics, I needed to author my own container, but these were excellent dockerfile guides: [Torch with CUDA](https://hub.docker.com/r/kaixhin/cuda-torch/~/dockerfile/) and it's [dependencies](https://hub.docker.com/r/kaixhin/cuda-torch-deps/~/dockerfile/). Also [Torch install](https://github.com/torch/distro) is a good reference.

[![29-Aug-2016-04-13-54](images/29-Aug-2016-04-13-54.jpg)](http://theludwigs.com/2016/08/weekend-software-experiment-facebooks-deepmask/29-aug-2016-04-13-54/)

First results in the picture. Did a nice job on this image for the large objects. The biggest problem I had was running out of GPU memory. The machine I was using only had 4G of video ram and this constrains how large an image you can feed in. We had a bunch of 4K x 3K street images, I found that scaling them down to 756x567 allowed me to get them thru the classifier. My modified classifier that implements a size limit is [here](https://gist.github.com/jhludwig/9d17d8c7abd2822f863ca8256ec3a82f)

The classifier is slow, seconds to tag an image. It would be interesting to keep it resident as a demon, and to just emit the metadata instead of a modified image, and see if I could get a higher framerate. Also I want to play around with both a faster video card, as well as maybe an opencl implementation to get to non-cuda platforms. This is also my first lua code ever, I have no idea which part of this code is fast or slow.

This was a fun little project. It points out that, if software is eating the world, then ML is eating software. For a certain class of problems, a fairly generic neural net plus a dataset is going to be competitive with the best laboriously hand-coded algorithm.
